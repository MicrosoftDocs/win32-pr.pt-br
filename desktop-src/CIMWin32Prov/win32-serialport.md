---
description: A \_ classe WMI SerialPort do Win32 representa uma porta serial em um sistema de computador executando o Windows.
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Classe Win32_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088934"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="8584c-103">\_Classe SerialPort Win32</span><span class="sxs-lookup"><span data-stu-id="8584c-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="8584c-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPort do Win32** representa uma porta serial em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="8584c-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="8584c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8584c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8584c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8584c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8584c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8584c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="8584c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8584c-108">Members</span></span>

<span data-ttu-id="8584c-109">A **classe \_ SerialPort do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8584c-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="8584c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8584c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8584c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8584c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8584c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8584c-112">Methods</span></span>

<span data-ttu-id="8584c-113">A **classe \_ SerialPort do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8584c-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="8584c-114">Método</span><span class="sxs-lookup"><span data-stu-id="8584c-114">Method</span></span>            | <span data-ttu-id="8584c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8584c-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8584c-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="8584c-116">**Reset**</span></span>         | <span data-ttu-id="8584c-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="8584c-117">Not implemented.</span></span> <span data-ttu-id="8584c-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="8584c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8584c-119">**SetPowerState**</span></span> | <span data-ttu-id="8584c-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="8584c-120">Not implemented.</span></span> <span data-ttu-id="8584c-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8584c-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8584c-122">Properties</span></span>

<span data-ttu-id="8584c-123">A **classe \_ SerialPort do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8584c-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8584c-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="8584c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8584c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="8584c-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-128">Availability and status of the device.</span></span>

<span data-ttu-id="8584c-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8584c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8584c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8584c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8584c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8584c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="8584c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="8584c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8584c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="8584c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8584c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="8584c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8584c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="8584c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8584c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="8584c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8584c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="8584c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8584c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="8584c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8584c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="8584c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8584c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="8584c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8584c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="8584c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8584c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="8584c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8584c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8584c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="8584c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="8584c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8584c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="8584c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8584c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="8584c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8584c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="8584c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="8584c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8584c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="8584c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="8584c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8584c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="8584c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="8584c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8584c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="8584c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="8584c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8584c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="8584c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="8584c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-160">**Binary**</span><span class="sxs-lookup"><span data-stu-id="8584c-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-161">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-163">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="8584c-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-164">Se for **true**, a porta serial será configurada para transferência de dados binários.</span><span class="sxs-lookup"><span data-stu-id="8584c-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="8584c-165">Como a API do Windows não dá suporte a transferências de modo não binário, essa propriedade deve ser **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="8584c-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-166">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="8584c-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-167">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8584c-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8584c-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-169">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Portas seriais DMTF \| 4,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8584c-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-170">Matriz de compatibilidade em nível de chip para o controlador serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="8584c-171">Esta propriedade descreve o buffer e outros recursos do controlador serial que podem ser inerentes ao hardware do chip.</span><span class="sxs-lookup"><span data-stu-id="8584c-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="8584c-172">A propriedade é um inteiro enumerado.</span><span class="sxs-lookup"><span data-stu-id="8584c-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="8584c-173">Essa propriedade é herdada do [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8584c-174">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8584c-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8584c-175">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8584c-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="8584c-176">**XT/at compatível** (3)</span><span class="sxs-lookup"><span data-stu-id="8584c-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="8584c-177">**compatível com 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="8584c-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="8584c-178">**compatível com 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="8584c-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="8584c-179">**compatível com 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="8584c-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="8584c-180">**compatível com 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="8584c-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="8584c-181">**compatível com 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="8584c-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-182">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8584c-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-183">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8584c-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-185">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM SerialController**](cim-serialcontroller.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="8584c-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-186">Matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do controlador serial indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="8584c-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="8584c-187">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="8584c-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="8584c-188">Essa propriedade é herdada do [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-189">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8584c-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-192">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8584c-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-193">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8584c-193">Short description of the object.</span></span>

<span data-ttu-id="8584c-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8584c-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-196">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8584c-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-198">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8584c-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-199">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8584c-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8584c-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8584c-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="8584c-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8584c-202"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="8584c-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-203">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8584c-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="8584c-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8584c-205">(1)</span><span class="sxs-lookup"><span data-stu-id="8584c-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-206">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8584c-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8584c-208">(2)</span><span class="sxs-lookup"><span data-stu-id="8584c-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8584c-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="8584c-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8584c-210">(3)</span><span class="sxs-lookup"><span data-stu-id="8584c-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-211">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="8584c-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8584c-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="8584c-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8584c-213">(4)</span><span class="sxs-lookup"><span data-stu-id="8584c-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-214">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-214">Device is not working properly.</span></span> <span data-ttu-id="8584c-215">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="8584c-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8584c-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="8584c-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8584c-217">(5)</span><span class="sxs-lookup"><span data-stu-id="8584c-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-218">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="8584c-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8584c-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="8584c-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8584c-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="8584c-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-221">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8584c-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8584c-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="8584c-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8584c-223">(7)</span><span class="sxs-lookup"><span data-stu-id="8584c-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8584c-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="8584c-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8584c-225">(8)</span><span class="sxs-lookup"><span data-stu-id="8584c-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-226">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="8584c-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8584c-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="8584c-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8584c-228">(9)</span><span class="sxs-lookup"><span data-stu-id="8584c-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-229">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-229">Device is not working properly.</span></span> <span data-ttu-id="8584c-230">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8584c-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="8584c-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8584c-232">(10)</span><span class="sxs-lookup"><span data-stu-id="8584c-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-233">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8584c-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="8584c-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8584c-235">(11)</span><span class="sxs-lookup"><span data-stu-id="8584c-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-236">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8584c-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="8584c-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8584c-238">12</span><span class="sxs-lookup"><span data-stu-id="8584c-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-239">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="8584c-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8584c-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8584c-241">(13)</span><span class="sxs-lookup"><span data-stu-id="8584c-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-242">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8584c-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="8584c-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8584c-244">(14)</span><span class="sxs-lookup"><span data-stu-id="8584c-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-245">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="8584c-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8584c-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="8584c-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8584c-247">(15)</span><span class="sxs-lookup"><span data-stu-id="8584c-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-248">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="8584c-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8584c-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="8584c-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8584c-250">(16)</span><span class="sxs-lookup"><span data-stu-id="8584c-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-251">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="8584c-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8584c-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="8584c-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8584c-253">(17)</span><span class="sxs-lookup"><span data-stu-id="8584c-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-254">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8584c-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8584c-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8584c-256">(18)</span><span class="sxs-lookup"><span data-stu-id="8584c-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-257">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="8584c-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8584c-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="8584c-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8584c-259">(19)</span><span class="sxs-lookup"><span data-stu-id="8584c-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8584c-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="8584c-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8584c-261">(20)</span><span class="sxs-lookup"><span data-stu-id="8584c-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-262">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="8584c-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8584c-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8584c-264">(21)</span><span class="sxs-lookup"><span data-stu-id="8584c-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-265">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="8584c-265">System failure.</span></span> <span data-ttu-id="8584c-266">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="8584c-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8584c-267">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8584c-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="8584c-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8584c-269">(22)</span><span class="sxs-lookup"><span data-stu-id="8584c-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-270">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8584c-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8584c-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="8584c-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8584c-272">(23)</span><span class="sxs-lookup"><span data-stu-id="8584c-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-273">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="8584c-273">System failure.</span></span> <span data-ttu-id="8584c-274">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="8584c-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8584c-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="8584c-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8584c-276">(24)</span><span class="sxs-lookup"><span data-stu-id="8584c-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-277">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="8584c-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8584c-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8584c-279">(25)</span><span class="sxs-lookup"><span data-stu-id="8584c-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-280">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8584c-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8584c-282">(26)</span><span class="sxs-lookup"><span data-stu-id="8584c-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-283">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8584c-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8584c-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="8584c-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8584c-285">(27)</span><span class="sxs-lookup"><span data-stu-id="8584c-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-286">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="8584c-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8584c-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="8584c-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8584c-288">(28)</span><span class="sxs-lookup"><span data-stu-id="8584c-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-289">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="8584c-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8584c-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="8584c-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8584c-291">(29)</span><span class="sxs-lookup"><span data-stu-id="8584c-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-292">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8584c-292">Device is disabled.</span></span> <span data-ttu-id="8584c-293">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="8584c-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8584c-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="8584c-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8584c-295">(30)</span><span class="sxs-lookup"><span data-stu-id="8584c-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-296">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="8584c-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8584c-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8584c-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8584c-298">(31)</span><span class="sxs-lookup"><span data-stu-id="8584c-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-299">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-299">Device is not working properly.</span></span> <span data-ttu-id="8584c-300">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="8584c-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8584c-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-302">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-304">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8584c-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-305">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8584c-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8584c-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8584c-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-310">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8584c-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8584c-311">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="8584c-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8584c-312">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="8584c-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8584c-313">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-314">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8584c-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-317">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="8584c-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-318">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8584c-318">Description of the object.</span></span>

<span data-ttu-id="8584c-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8584c-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-323">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="8584c-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-324">Identificador exclusivo da porta serial com outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="8584c-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="8584c-325">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8584c-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-327">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8584c-329">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="8584c-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="8584c-330">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8584c-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8584c-334">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="8584c-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="8584c-335">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8584c-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-337">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8584c-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-339">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="8584c-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-340">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8584c-340">Date and time the object was installed.</span></span> <span data-ttu-id="8584c-341">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8584c-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8584c-342">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-343">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8584c-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-344">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8584c-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8584c-346">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8584c-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8584c-347">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-348">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="8584c-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-349">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8584c-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-351">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Portas seriais DMTF \| 4,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits por segundo ")</span><span class="sxs-lookup"><span data-stu-id="8584c-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-352">Taxa de transmissão máxima (em bits por segundo) suportada pelo controlador serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="8584c-353">Essa propriedade é herdada do [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-354">**MaximumInputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="8584c-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-355">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8584c-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-357">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxRxQueue"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8584c-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-358">Tamanho máximo do buffer de entrada interno do driver de porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="8584c-359">Um valor de 0 (zero) indica que nenhum valor máximo é imposto pelo provedor serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-360">**MaximumOutputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="8584c-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-361">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8584c-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-363">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxTxQueue"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8584c-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-364">Tamanho máximo do buffer de saída interno do driver de porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="8584c-365">Um valor de 0 (zero) indica que nenhum valor máximo é imposto pelo provedor serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-366">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="8584c-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-367">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8584c-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-369">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="8584c-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-370">Número máximo de entidades diretamente endereçáveis com suporte por este controlador.</span><span class="sxs-lookup"><span data-stu-id="8584c-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="8584c-371">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8584c-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="8584c-372">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8584c-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-376">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8584c-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-377">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8584c-377">Label by which the object is known.</span></span> <span data-ttu-id="8584c-378">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="8584c-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="8584c-379">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-380">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="8584c-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-381">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-383">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema de descrição de hardware \\ \\ \\ \\ \\ \\ MultifunctionAdapter")</span><span class="sxs-lookup"><span data-stu-id="8584c-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-384">Se **for true**, as instâncias dessa classe foram descobertas automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8584c-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="8584c-385">Se, por exemplo, o hardware foi adicionado por meio do painel de controle, o sistema operacional localiza instâncias dessa classe consultando o hardware das instâncias desta classe.</span><span class="sxs-lookup"><span data-stu-id="8584c-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8584c-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-389">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8584c-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-390">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8584c-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="8584c-391">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8584c-392">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8584c-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="8584c-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8584c-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-394">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8584c-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8584c-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8584c-396">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8584c-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8584c-397">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="8584c-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8584c-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8584c-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8584c-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="8584c-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8584c-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8584c-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8584c-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8584c-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-402">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8584c-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8584c-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="8584c-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-404">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="8584c-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8584c-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="8584c-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-406">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="8584c-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8584c-407">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="8584c-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8584c-408">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8584c-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="8584c-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-410">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="8584c-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8584c-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="8584c-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-412">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="8584c-412">Timed Power-On Supported</span></span>

<span data-ttu-id="8584c-413">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="8584c-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-414">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8584c-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-415">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8584c-417">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="8584c-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="8584c-418">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="8584c-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="8584c-419">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-420">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="8584c-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-421">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8584c-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-423">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="8584c-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-424">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="8584c-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="8584c-425">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="8584c-426">A lista a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8584c-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8584c-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8584c-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8584c-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8584c-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="8584c-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="8584c-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="8584c-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="8584c-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="8584c-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="8584c-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="8584c-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="8584c-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8584c-433">ATA ou ATAPI</span><span class="sxs-lookup"><span data-stu-id="8584c-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="8584c-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="8584c-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="8584c-435"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="8584c-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="8584c-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="8584c-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="8584c-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="8584c-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="8584c-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="8584c-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="8584c-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="8584c-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="8584c-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="8584c-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="8584c-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="8584c-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="8584c-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="8584c-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="8584c-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="8584c-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="8584c-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="8584c-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="8584c-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="8584c-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="8584c-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="8584c-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="8584c-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="8584c-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="8584c-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="8584c-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="8584c-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="8584c-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="8584c-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="8584c-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="8584c-451"><span id="VME"></span><span id="vme"></span>**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="8584c-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="8584c-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="8584c-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="8584c-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="8584c-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="8584c-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="8584c-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="8584c-455"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="8584c-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="8584c-456"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="8584c-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="8584c-457"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="8584c-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="8584c-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="8584c-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="8584c-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="8584c-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="8584c-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="8584c-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="8584c-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="8584c-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="8584c-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="8584c-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="8584c-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="8584c-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="8584c-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="8584c-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="8584c-465"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="8584c-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="8584c-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="8584c-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="8584c-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="8584c-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="8584c-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="8584c-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="8584c-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="8584c-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="8584c-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="8584c-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="8584c-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="8584c-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="8584c-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="8584c-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="8584c-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="8584c-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="8584c-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="8584c-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="8584c-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-476">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-478">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvSubType")</span><span class="sxs-lookup"><span data-stu-id="8584c-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-479">Tipo de provedor de comunicações.</span><span class="sxs-lookup"><span data-stu-id="8584c-479">Communications provider type.</span></span>

<span data-ttu-id="8584c-480">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="8584c-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="8584c-481">"Dispositivo de FAX"</span><span class="sxs-lookup"><span data-stu-id="8584c-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="8584c-482">"Protocolo LAT"</span><span class="sxs-lookup"><span data-stu-id="8584c-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="8584c-483">"Dispositivo de modem"</span><span class="sxs-lookup"><span data-stu-id="8584c-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="8584c-484">"Ponte de rede"</span><span class="sxs-lookup"><span data-stu-id="8584c-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="8584c-485">"Porta paralela"</span><span class="sxs-lookup"><span data-stu-id="8584c-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="8584c-486">"Porta serial RS232"</span><span class="sxs-lookup"><span data-stu-id="8584c-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="8584c-487">"Porta RS422"</span><span class="sxs-lookup"><span data-stu-id="8584c-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="8584c-488">"Porta RS423"</span><span class="sxs-lookup"><span data-stu-id="8584c-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="8584c-489">"Porta RS449"</span><span class="sxs-lookup"><span data-stu-id="8584c-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="8584c-490">"Dispositivo de scanner"</span><span class="sxs-lookup"><span data-stu-id="8584c-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="8584c-491">"TelNet TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="8584c-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="8584c-492">"X. 25"</span><span class="sxs-lookup"><span data-stu-id="8584c-492">"X.25"</span></span></dd> <dd><span data-ttu-id="8584c-493">Não especificado</span><span class="sxs-lookup"><span data-stu-id="8584c-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="8584c-494">**Dispositivo de fax** ("dispositivo de fax")</span><span class="sxs-lookup"><span data-stu-id="8584c-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="8584c-495">**Protocolo Lat** ("protocolo Lat")</span><span class="sxs-lookup"><span data-stu-id="8584c-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="8584c-496">**Dispositivo de modem** ("dispositivo de modem")</span><span class="sxs-lookup"><span data-stu-id="8584c-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="8584c-497">**Ponte de rede** ("ponte de rede")</span><span class="sxs-lookup"><span data-stu-id="8584c-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="8584c-498">**Porta paralela** ("porta paralela")</span><span class="sxs-lookup"><span data-stu-id="8584c-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="8584c-499">**Porta serial RS232** ("porta serial RS232")</span><span class="sxs-lookup"><span data-stu-id="8584c-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="8584c-500">**Porta RS422** ("porta RS422")</span><span class="sxs-lookup"><span data-stu-id="8584c-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="8584c-501">**Porta RS423** ("porta RS423")</span><span class="sxs-lookup"><span data-stu-id="8584c-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="8584c-502">**Porta RS449** ("porta RS449")</span><span class="sxs-lookup"><span data-stu-id="8584c-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="8584c-503">**Dispositivo de scanner** ("dispositivo de scanner")</span><span class="sxs-lookup"><span data-stu-id="8584c-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="8584c-504">**Telnet TCP/IP** ("Telnet TCP/IP")</span><span class="sxs-lookup"><span data-stu-id="8584c-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="8584c-505">**X. 25** ("X. 25")</span><span class="sxs-lookup"><span data-stu-id="8584c-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="8584c-506">**Não especificado** ("não especificado")</span><span class="sxs-lookup"><span data-stu-id="8584c-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-507">**SettableBaudRate**</span><span class="sxs-lookup"><span data-stu-id="8584c-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-508">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-510">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ baud")</span><span class="sxs-lookup"><span data-stu-id="8584c-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-511">Se **for true**, a taxa de transmissão poderá ser alterada para essa porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-512">**SettableDataBits**</span><span class="sxs-lookup"><span data-stu-id="8584c-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-513">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-515">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ DataBits")</span><span class="sxs-lookup"><span data-stu-id="8584c-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-516">Se **for true**, os bits de dados poderão ser definidos para essa porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-517">**SettableFlowControl**</span><span class="sxs-lookup"><span data-stu-id="8584c-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-518">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-520">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ handshake")</span><span class="sxs-lookup"><span data-stu-id="8584c-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-521">Se **for true**, o controle de fluxo poderá ser definido para essa porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-522">**SettableParity**</span><span class="sxs-lookup"><span data-stu-id="8584c-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-523">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-525">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ Parity")</span><span class="sxs-lookup"><span data-stu-id="8584c-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-526">Se **for true**, a paridade poderá ser definida para essa porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-527">**SettableParityCheck**</span><span class="sxs-lookup"><span data-stu-id="8584c-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-528">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-529">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-530">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ Parity \_ check")</span><span class="sxs-lookup"><span data-stu-id="8584c-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-531">Se **for true**, a verificação de paridade poderá ser definida para essa porta serial (se houver suporte para a verificação de paridade).</span><span class="sxs-lookup"><span data-stu-id="8584c-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-532">**SettableRLSD**</span><span class="sxs-lookup"><span data-stu-id="8584c-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-533">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-534">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-535">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="8584c-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-536">Se **verdadeiro**, a RLSD (detecção de sinal de linha) recebida pode ser definida para esta porta serial (se houver suporte para RLSD).</span><span class="sxs-lookup"><span data-stu-id="8584c-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-537">**SettableStopBits**</span><span class="sxs-lookup"><span data-stu-id="8584c-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-538">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-539">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-540">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ STOPBITS")</span><span class="sxs-lookup"><span data-stu-id="8584c-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-541">Se **for true**, os bits de parada poderão ser definidos para essa porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-542">**Status**</span><span class="sxs-lookup"><span data-stu-id="8584c-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-543">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-544">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-545">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="8584c-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-546">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8584c-546">Current status of the object.</span></span> <span data-ttu-id="8584c-547">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="8584c-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8584c-548">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8584c-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8584c-549">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8584c-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8584c-550">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8584c-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8584c-551">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8584c-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8584c-552">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8584c-553">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8584c-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8584c-554">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8584c-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8584c-555">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="8584c-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8584c-556">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8584c-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8584c-557">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8584c-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8584c-558">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8584c-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8584c-559">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8584c-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8584c-560">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="8584c-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8584c-561">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="8584c-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8584c-562">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="8584c-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8584c-563">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8584c-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8584c-564">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="8584c-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8584c-565">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="8584c-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8584c-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-567">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8584c-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-568">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-569">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="8584c-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-570">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8584c-570">State of the logical device.</span></span> <span data-ttu-id="8584c-571">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="8584c-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8584c-572">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8584c-573">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8584c-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8584c-574">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8584c-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8584c-575">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8584c-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8584c-576">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="8584c-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8584c-577">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="8584c-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8584c-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="8584c-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-579">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-580">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-581">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ 16BITMODE")</span><span class="sxs-lookup"><span data-stu-id="8584c-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-582">Se for **true**, o modo de 16 bits terá suporte nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-583">**SupportsDTRDSR**</span><span class="sxs-lookup"><span data-stu-id="8584c-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-584">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-585">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-586">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ DTRDSR")</span><span class="sxs-lookup"><span data-stu-id="8584c-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-587">Se for **verdadeiro**, os sinais de DTR (Data Terminal Ready) e Data Set Ready (DSR) têm suporte nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-588">**SupportsElapsedTimeouts**</span><span class="sxs-lookup"><span data-stu-id="8584c-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-589">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-590">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-591">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ TOTALTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="8584c-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-592">Se **verdadeiro**, os tempos limite decorridos têm suporte nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="8584c-593">Tempos limite decorridos acompanham a quantidade total de tempo entre as transmissões de dados.</span><span class="sxs-lookup"><span data-stu-id="8584c-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-594">**SupportsIntTimeouts**</span><span class="sxs-lookup"><span data-stu-id="8584c-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-595">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-596">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-597">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ INTTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="8584c-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-598">Se **for true**, haverá suporte para tempos limite de intervalo.</span><span class="sxs-lookup"><span data-stu-id="8584c-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="8584c-599">Um tempo limite de intervalo é a quantidade de tempo permitido para decorrer entre a chegada de cada parte dos dados.</span><span class="sxs-lookup"><span data-stu-id="8584c-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-600">**SupportsParityCheck**</span><span class="sxs-lookup"><span data-stu-id="8584c-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-601">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-602">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-603">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF de verificação de \_ paridade \_ ")</span><span class="sxs-lookup"><span data-stu-id="8584c-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-604">Se for **true**, haverá suporte para a verificação de paridade nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-605">**SupportsRLSD**</span><span class="sxs-lookup"><span data-stu-id="8584c-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-606">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-607">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-608">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="8584c-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-609">Se **verdadeiro**, a RLSD (detecção de sinal de linha) recebida tem suporte nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-610">**SupportsRTSCTS**</span><span class="sxs-lookup"><span data-stu-id="8584c-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-611">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-612">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-613">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RTSCTS")</span><span class="sxs-lookup"><span data-stu-id="8584c-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-614">Se for **verdadeiro**, os sinais de RTS (pronto para enviar) e não criptografar para enviar (CTS) têm suporte nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-615">**SupportsSpecialCharacters**</span><span class="sxs-lookup"><span data-stu-id="8584c-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-616">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-617">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-618">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SPECIALCHARS")</span><span class="sxs-lookup"><span data-stu-id="8584c-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-619">Se **for true**, os caracteres de controle de porta serial têm suporte.</span><span class="sxs-lookup"><span data-stu-id="8584c-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="8584c-620">Esses caracteres sinalizam eventos em vez de dados.</span><span class="sxs-lookup"><span data-stu-id="8584c-620">These characters signal events rather than data.</span></span> <span data-ttu-id="8584c-621">Esses caracteres não são exibíveis e são definidos pelo driver.</span><span class="sxs-lookup"><span data-stu-id="8584c-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="8584c-622">Eles incluem EofChar, ErrorChar, BreakChar, EventChar, XonChar e XoffChar.</span><span class="sxs-lookup"><span data-stu-id="8584c-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-623">**SupportsXOnXOff**</span><span class="sxs-lookup"><span data-stu-id="8584c-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-624">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-625">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-626">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ XONXOFF")</span><span class="sxs-lookup"><span data-stu-id="8584c-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-627">Se for **true**, o controle de fluxo XON ou XOFF terá suporte nesta porta serial.</span><span class="sxs-lookup"><span data-stu-id="8584c-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-628">**SupportsXOnXOffSet**</span><span class="sxs-lookup"><span data-stu-id="8584c-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-629">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8584c-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-630">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-631">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SETXCHAR")</span><span class="sxs-lookup"><span data-stu-id="8584c-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="8584c-632">Se **for true**, o provedor de comunicações dará suporte à configuração da configuração de controle de fluxo XONor XOFF.</span><span class="sxs-lookup"><span data-stu-id="8584c-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="8584c-633">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8584c-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-634">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-635">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-636">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8584c-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8584c-637">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="8584c-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="8584c-638">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-639">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8584c-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-640">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8584c-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-641">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8584c-642">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8584c-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8584c-643">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8584c-643">Name of the scoping system.</span></span>

<span data-ttu-id="8584c-644">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8584c-645">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="8584c-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8584c-646">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8584c-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8584c-647">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8584c-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8584c-648">Data e hora da última redefinição deste controlador.</span><span class="sxs-lookup"><span data-stu-id="8584c-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="8584c-649">Isso pode significar que o controlador estava desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="8584c-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="8584c-650">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8584c-651">Comentários</span><span class="sxs-lookup"><span data-stu-id="8584c-651">Remarks</span></span>

<span data-ttu-id="8584c-652">A **classe \_ SerialPort do Win32** é derivada do [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8584c-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8584c-653">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8584c-653">Examples</span></span>

<span data-ttu-id="8584c-654">Para obter um método alternativo de recuperação de informações de porta serial (do registro), consulte o exemplo [enumerar portas](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8584c-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="8584c-655">O exemplo do PowerShell [listar Propriedades de portas seriais](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) retorna informações sobre as portas de série instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="8584c-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="8584c-656">O exemplo de VBScript a seguir retorna informações sobre as portas de série instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="8584c-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="8584c-657">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8584c-657">Requirements</span></span>



| <span data-ttu-id="8584c-658">Requisito</span><span class="sxs-lookup"><span data-stu-id="8584c-658">Requirement</span></span> | <span data-ttu-id="8584c-659">Valor</span><span class="sxs-lookup"><span data-stu-id="8584c-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8584c-660">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8584c-660">Minimum supported client</span></span><br/> | <span data-ttu-id="8584c-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8584c-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8584c-662">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8584c-662">Minimum supported server</span></span><br/> | <span data-ttu-id="8584c-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8584c-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8584c-664">Namespace</span><span class="sxs-lookup"><span data-stu-id="8584c-664">Namespace</span></span><br/>                | <span data-ttu-id="8584c-665">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8584c-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8584c-666">MOF</span><span class="sxs-lookup"><span data-stu-id="8584c-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8584c-667"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8584c-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8584c-668">DLL</span><span class="sxs-lookup"><span data-stu-id="8584c-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8584c-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8584c-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8584c-670">Confira também</span><span class="sxs-lookup"><span data-stu-id="8584c-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8584c-671">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="8584c-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="8584c-672">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8584c-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
