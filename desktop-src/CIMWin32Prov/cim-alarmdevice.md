---
description: A \_ classe CIM AlarmDevice é um dispositivo de alarme que emite indicações audíveis ou visíveis relacionadas a uma situação de problema.
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: Classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501011"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="7985c-103">\_Classe CIM AlarmDevice</span><span class="sxs-lookup"><span data-stu-id="7985c-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="7985c-104">A classe **CIM \_ AlarmDevice** é um dispositivo de alarme que emite indicações audíveis ou visíveis relacionadas a uma situação de problema.</span><span class="sxs-lookup"><span data-stu-id="7985c-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="7985c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7985c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7985c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="7985c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7985c-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="7985c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7985c-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7985c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7985c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7985c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="7985c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="7985c-110">Members</span></span>

<span data-ttu-id="7985c-111">A classe **CIM \_ AlarmDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7985c-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="7985c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7985c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7985c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7985c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7985c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="7985c-114">Methods</span></span>

<span data-ttu-id="7985c-115">A classe **CIM \_ AlarmDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7985c-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="7985c-116">Método</span><span class="sxs-lookup"><span data-stu-id="7985c-116">Method</span></span>                                                                 | <span data-ttu-id="7985c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7985c-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7985c-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="7985c-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="7985c-119">Solicita uma redefinição de dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7985c-119">Requests a logical device reset.</span></span> <span data-ttu-id="7985c-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="7985c-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="7985c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7985c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="7985c-122">Define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="7985c-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="7985c-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="7985c-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="7985c-124">**Seturgência**</span><span class="sxs-lookup"><span data-stu-id="7985c-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="7985c-125">Define o nível de urgência desejado para o alarme.</span><span class="sxs-lookup"><span data-stu-id="7985c-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="7985c-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="7985c-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="7985c-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7985c-127">Properties</span></span>

<span data-ttu-id="7985c-128">A classe **CIM \_ AlarmDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7985c-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7985c-129">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="7985c-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7985c-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-132">Se for **true**, o alarme será audível.</span><span class="sxs-lookup"><span data-stu-id="7985c-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="7985c-133">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="7985c-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7985c-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-136">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7985c-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-137">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7985c-137">Availability and status of the device.</span></span>

<span data-ttu-id="7985c-138">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7985c-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7985c-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7985c-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="7985c-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7985c-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="7985c-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7985c-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="7985c-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7985c-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="7985c-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7985c-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="7985c-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7985c-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="7985c-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7985c-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="7985c-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7985c-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="7985c-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7985c-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="7985c-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7985c-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="7985c-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7985c-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="7985c-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7985c-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="7985c-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-152">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7985c-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7985c-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="7985c-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-154">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="7985c-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7985c-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="7985c-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-156">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="7985c-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7985c-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="7985c-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7985c-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="7985c-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-159">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="7985c-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7985c-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="7985c-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-161">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="7985c-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7985c-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="7985c-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-163">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="7985c-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7985c-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="7985c-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-165">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="7985c-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7985c-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="7985c-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-167">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="7985c-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7985c-168">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="7985c-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-171">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7985c-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-172">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7985c-172">A short textual description of the object.</span></span>

<span data-ttu-id="7985c-173">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7985c-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-175">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7985c-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-177">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7985c-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-178">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7985c-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7985c-179">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7985c-180">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="7985c-180">**This device is working properly.**</span></span> <span data-ttu-id="7985c-181"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="7985c-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7985c-182">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="7985c-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="7985c-183">(1)</span><span class="sxs-lookup"><span data-stu-id="7985c-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7985c-184">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7985c-185">(2)</span><span class="sxs-lookup"><span data-stu-id="7985c-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7985c-186">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="7985c-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7985c-187">(3)</span><span class="sxs-lookup"><span data-stu-id="7985c-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7985c-188">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="7985c-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7985c-189">(4)</span><span class="sxs-lookup"><span data-stu-id="7985c-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7985c-190">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="7985c-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7985c-191">(5)</span><span class="sxs-lookup"><span data-stu-id="7985c-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7985c-192">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="7985c-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7985c-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="7985c-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7985c-194">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="7985c-194">**Cannot filter.**</span></span> <span data-ttu-id="7985c-195">(7)</span><span class="sxs-lookup"><span data-stu-id="7985c-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7985c-196">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="7985c-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7985c-197">(8)</span><span class="sxs-lookup"><span data-stu-id="7985c-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7985c-198">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="7985c-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7985c-199">(9)</span><span class="sxs-lookup"><span data-stu-id="7985c-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7985c-200">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="7985c-200">**This device cannot start.**</span></span> <span data-ttu-id="7985c-201">(10)</span><span class="sxs-lookup"><span data-stu-id="7985c-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7985c-202">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="7985c-202">**This device failed.**</span></span> <span data-ttu-id="7985c-203">(11)</span><span class="sxs-lookup"><span data-stu-id="7985c-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7985c-204">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="7985c-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7985c-205">12</span><span class="sxs-lookup"><span data-stu-id="7985c-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7985c-206">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7985c-207">(13)</span><span class="sxs-lookup"><span data-stu-id="7985c-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7985c-208">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="7985c-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7985c-209">(14)</span><span class="sxs-lookup"><span data-stu-id="7985c-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7985c-210">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="7985c-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7985c-211">(15)</span><span class="sxs-lookup"><span data-stu-id="7985c-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7985c-212">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="7985c-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7985c-213">(16)</span><span class="sxs-lookup"><span data-stu-id="7985c-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7985c-214">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="7985c-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7985c-215">(17)</span><span class="sxs-lookup"><span data-stu-id="7985c-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7985c-216">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7985c-217">(18)</span><span class="sxs-lookup"><span data-stu-id="7985c-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7985c-218">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="7985c-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="7985c-219">(19)</span><span class="sxs-lookup"><span data-stu-id="7985c-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7985c-220">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="7985c-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="7985c-221">(20)</span><span class="sxs-lookup"><span data-stu-id="7985c-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7985c-222">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7985c-223">(21)</span><span class="sxs-lookup"><span data-stu-id="7985c-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7985c-224">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="7985c-224">**This device is disabled.**</span></span> <span data-ttu-id="7985c-225">(22)</span><span class="sxs-lookup"><span data-stu-id="7985c-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7985c-226">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="7985c-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7985c-227">(23)</span><span class="sxs-lookup"><span data-stu-id="7985c-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7985c-228">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="7985c-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7985c-229">(24)</span><span class="sxs-lookup"><span data-stu-id="7985c-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7985c-230">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7985c-231">(25)</span><span class="sxs-lookup"><span data-stu-id="7985c-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7985c-232">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7985c-233">(26)</span><span class="sxs-lookup"><span data-stu-id="7985c-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7985c-234">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="7985c-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7985c-235">(27)</span><span class="sxs-lookup"><span data-stu-id="7985c-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7985c-236">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="7985c-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7985c-237">(28)</span><span class="sxs-lookup"><span data-stu-id="7985c-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7985c-238">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="7985c-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7985c-239">(29)</span><span class="sxs-lookup"><span data-stu-id="7985c-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7985c-240">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="7985c-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7985c-241">(30)</span><span class="sxs-lookup"><span data-stu-id="7985c-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7985c-242">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7985c-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7985c-243">(31)</span><span class="sxs-lookup"><span data-stu-id="7985c-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7985c-244">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7985c-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7985c-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-247">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7985c-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-248">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7985c-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7985c-249">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-250">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7985c-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-253">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7985c-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7985c-254">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="7985c-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7985c-255">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="7985c-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7985c-256">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-257">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7985c-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-260">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="7985c-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-261">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7985c-261">A textual description of the object.</span></span>

<span data-ttu-id="7985c-262">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-263">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7985c-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-266">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7985c-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7985c-267">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7985c-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7985c-268">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-269">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7985c-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-270">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7985c-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-272">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="7985c-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7985c-273">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7985c-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-277">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="7985c-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7985c-278">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7985c-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-280">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7985c-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-282">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="7985c-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-283">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="7985c-283">Indicates when the object was installed.</span></span> <span data-ttu-id="7985c-284">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="7985c-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7985c-285">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-286">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7985c-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-287">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7985c-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-289">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7985c-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7985c-290">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-291">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7985c-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-294">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7985c-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-295">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="7985c-295">Label by which the object is known.</span></span> <span data-ttu-id="7985c-296">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="7985c-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7985c-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7985c-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-301">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7985c-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-302">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7985c-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7985c-303">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7985c-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="7985c-304">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-305">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7985c-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-306">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7985c-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7985c-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-308">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7985c-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="7985c-309">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7985c-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7985c-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-311">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="7985c-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7985c-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="7985c-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-313">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7985c-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7985c-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="7985c-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-315">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="7985c-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7985c-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7985c-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-317">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7985c-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7985c-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="7985c-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-319">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="7985c-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7985c-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="7985c-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-321">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="7985c-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="7985c-322">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="7985c-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="7985c-323">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7985c-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7985c-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="7985c-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-325">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="7985c-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7985c-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="7985c-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-327">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="7985c-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7985c-328">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7985c-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-329">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7985c-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-331">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="7985c-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7985c-332">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7985c-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7985c-333">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="7985c-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7985c-334">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7985c-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7985c-335">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-336">**Status**</span><span class="sxs-lookup"><span data-stu-id="7985c-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-339">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7985c-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-340">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7985c-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="7985c-341">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="7985c-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7985c-342">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="7985c-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7985c-343">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="7985c-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7985c-344">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="7985c-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7985c-345">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="7985c-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7985c-346">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="7985c-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7985c-347">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7985c-348">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7985c-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7985c-349">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7985c-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7985c-350">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="7985c-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7985c-351">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7985c-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7985c-352">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="7985c-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7985c-353">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7985c-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7985c-354">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="7985c-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7985c-355">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="7985c-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7985c-356">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="7985c-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7985c-357">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="7985c-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7985c-358">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7985c-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7985c-359">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="7985c-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7985c-360">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="7985c-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7985c-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7985c-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-362">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7985c-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-364">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="7985c-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7985c-365">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7985c-365">State of the logical device.</span></span> <span data-ttu-id="7985c-366">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="7985c-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="7985c-367">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7985c-368">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7985c-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7985c-369">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="7985c-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7985c-370">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7985c-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7985c-371">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="7985c-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7985c-372">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="7985c-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7985c-373">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7985c-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-376">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7985c-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7985c-377">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="7985c-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="7985c-378">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-379">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7985c-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-380">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7985c-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7985c-382">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7985c-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7985c-383">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="7985c-383">The scoping system's name.</span></span>

<span data-ttu-id="7985c-384">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7985c-385">**Urgência**</span><span class="sxs-lookup"><span data-stu-id="7985c-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-386">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7985c-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-388">Valor enumerado que indica a frequência relativa na qual o alarme pisca, vibra ou emite tons audíveis.</span><span class="sxs-lookup"><span data-stu-id="7985c-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7985c-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7985c-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-390">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7985c-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7985c-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7985c-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-392">Outros.</span><span class="sxs-lookup"><span data-stu-id="7985c-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7985c-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="7985c-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-394">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7985c-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="7985c-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informativo** (3)</span><span class="sxs-lookup"><span data-stu-id="7985c-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-396">Informativa.</span><span class="sxs-lookup"><span data-stu-id="7985c-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="7985c-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Não crítico** (4)</span><span class="sxs-lookup"><span data-stu-id="7985c-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-398">Não crítico.</span><span class="sxs-lookup"><span data-stu-id="7985c-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="7985c-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="7985c-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-400">Crítica.</span><span class="sxs-lookup"><span data-stu-id="7985c-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="7985c-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Irrecuperável** (6)</span><span class="sxs-lookup"><span data-stu-id="7985c-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7985c-402">Irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="7985c-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7985c-403">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="7985c-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7985c-404">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7985c-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7985c-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7985c-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7985c-406">Se for **true**, o alarme ficará visível.</span><span class="sxs-lookup"><span data-stu-id="7985c-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7985c-407">Comentários</span><span class="sxs-lookup"><span data-stu-id="7985c-407">Remarks</span></span>

<span data-ttu-id="7985c-408">A classe **CIM \_ AlarmDevice** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7985c-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7985c-409">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="7985c-409">WMI does not implement this class.</span></span>

<span data-ttu-id="7985c-410">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="7985c-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7985c-411">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="7985c-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7985c-412">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7985c-412">Requirements</span></span>



| <span data-ttu-id="7985c-413">Requisito</span><span class="sxs-lookup"><span data-stu-id="7985c-413">Requirement</span></span> | <span data-ttu-id="7985c-414">Valor</span><span class="sxs-lookup"><span data-stu-id="7985c-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7985c-415">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7985c-415">Minimum supported client</span></span><br/> | <span data-ttu-id="7985c-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7985c-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7985c-417">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7985c-417">Minimum supported server</span></span><br/> | <span data-ttu-id="7985c-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7985c-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7985c-419">Namespace</span><span class="sxs-lookup"><span data-stu-id="7985c-419">Namespace</span></span><br/>                | <span data-ttu-id="7985c-420">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7985c-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7985c-421">MOF</span><span class="sxs-lookup"><span data-stu-id="7985c-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7985c-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7985c-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7985c-423">DLL</span><span class="sxs-lookup"><span data-stu-id="7985c-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7985c-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7985c-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7985c-425">Confira também</span><span class="sxs-lookup"><span data-stu-id="7985c-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7985c-426">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7985c-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

