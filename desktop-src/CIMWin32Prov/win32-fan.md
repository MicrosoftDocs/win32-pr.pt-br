---
description: A \_ classe WMI de ventilador do Win32 representa as propriedades de um dispositivo de ventilador no sistema de computador. Por exemplo, o ventilador de resfriamento da CPU.
ms.assetid: ff48b788-d759-45cf-812f-a80dba0c9192
ms.tgt_platform: multiple
title: Classe Win32_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Fan
- Win32_Fan.Reset
- Win32_Fan.SetPowerState
- Win32_Fan.SetSpeed
- Win32_Fan.ActiveCooling
- Win32_Fan.Availability
- Win32_Fan.Caption
- Win32_Fan.ConfigManagerErrorCode
- Win32_Fan.ConfigManagerUserConfig
- Win32_Fan.CreationClassName
- Win32_Fan.Description
- Win32_Fan.DesiredSpeed
- Win32_Fan.DeviceID
- Win32_Fan.ErrorCleared
- Win32_Fan.ErrorDescription
- Win32_Fan.InstallDate
- Win32_Fan.LastErrorCode
- Win32_Fan.Name
- Win32_Fan.PNPDeviceID
- Win32_Fan.PowerManagementCapabilities
- Win32_Fan.PowerManagementSupported
- Win32_Fan.Status
- Win32_Fan.StatusInfo
- Win32_Fan.SystemCreationClassName
- Win32_Fan.SystemName
- Win32_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67f248b74fa665f30c9c3b9ffa51cb8cee5a5782
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500810"
---
# <a name="win32_fan-class"></a><span data-ttu-id="12540-104">\_Classe de ventilador Win32</span><span class="sxs-lookup"><span data-stu-id="12540-104">Win32\_Fan class</span></span>

<span data-ttu-id="12540-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ ventilador do Win32** representa as propriedades de um dispositivo de ventilador no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="12540-105">The **Win32\_Fan** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a fan device in the computer system.</span></span> <span data-ttu-id="12540-106">Por exemplo, o ventilador de resfriamento da CPU.</span><span class="sxs-lookup"><span data-stu-id="12540-106">For example, the CPU cooling fan.</span></span>

<span data-ttu-id="12540-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="12540-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="12540-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="12540-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12540-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12540-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB5-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Fan : CIM_Fan
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="12540-110">Membros</span><span class="sxs-lookup"><span data-stu-id="12540-110">Members</span></span>

<span data-ttu-id="12540-111">A classe de **\_ ventilador do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12540-111">The **Win32\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="12540-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="12540-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="12540-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12540-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12540-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="12540-114">Methods</span></span>

<span data-ttu-id="12540-115">A classe de **\_ ventilador do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="12540-115">The **Win32\_Fan** class has these methods.</span></span>



| <span data-ttu-id="12540-116">Método</span><span class="sxs-lookup"><span data-stu-id="12540-116">Method</span></span>            | <span data-ttu-id="12540-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="12540-117">Description</span></span>                                                                                                                                                                                  |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12540-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="12540-118">**Reset**</span></span>         | <span data-ttu-id="12540-119">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12540-119">Not implemented.</span></span> <span data-ttu-id="12540-120">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ ventilador do CIM**](cim-fan.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="12540-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="12540-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="12540-121">**SetPowerState**</span></span> | <span data-ttu-id="12540-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12540-122">Not implemented.</span></span> <span data-ttu-id="12540-123">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ ventilador do CIM**](cim-fan.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="12540-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/> |
| <span data-ttu-id="12540-124">**SETSPEED**</span><span class="sxs-lookup"><span data-stu-id="12540-124">**SetSpeed**</span></span>      | <span data-ttu-id="12540-125">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12540-125">Not implemented.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="12540-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12540-126">Properties</span></span>

<span data-ttu-id="12540-127">A classe de **\_ ventilador do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="12540-127">The **Win32\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12540-128">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="12540-128">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12540-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12540-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-131">Se **for true**, o dispositivo de resfriamento fornecerá o resfriamento ativo (em oposição ao passivo).</span><span class="sxs-lookup"><span data-stu-id="12540-131">If **True**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="12540-132">Essa propriedade é herdada do [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-132">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-133">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="12540-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12540-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12540-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-136">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="12540-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="12540-137">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-137">Availability and status of the device.</span></span>

<span data-ttu-id="12540-138">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12540-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="12540-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12540-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="12540-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="12540-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="12540-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="12540-142">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="12540-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="12540-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="12540-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="12540-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="12540-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12540-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="12540-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="12540-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="12540-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="12540-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="12540-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="12540-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="12540-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12540-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="12540-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="12540-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="12540-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="12540-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="12540-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="12540-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="12540-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="12540-153">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="12540-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="12540-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="12540-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="12540-155">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="12540-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="12540-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="12540-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="12540-157">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="12540-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="12540-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="12540-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="12540-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="12540-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="12540-160">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="12540-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="12540-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="12540-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="12540-162">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="12540-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="12540-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="12540-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="12540-164">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="12540-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="12540-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="12540-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="12540-166">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="12540-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="12540-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="12540-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="12540-168">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="12540-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12540-169">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="12540-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="12540-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="12540-173">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="12540-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="12540-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12540-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12540-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12540-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12540-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-178">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12540-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12540-179">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="12540-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="12540-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="12540-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="12540-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="12540-182"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="12540-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="12540-183">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12540-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="12540-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="12540-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="12540-185">(1)</span><span class="sxs-lookup"><span data-stu-id="12540-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="12540-186">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="12540-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12540-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="12540-188">(2)</span><span class="sxs-lookup"><span data-stu-id="12540-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="12540-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="12540-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="12540-190">(3)</span><span class="sxs-lookup"><span data-stu-id="12540-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="12540-191">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="12540-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12540-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="12540-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="12540-193">(4)</span><span class="sxs-lookup"><span data-stu-id="12540-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="12540-194">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12540-194">Device is not working properly.</span></span> <span data-ttu-id="12540-195">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="12540-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="12540-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="12540-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="12540-197">(5)</span><span class="sxs-lookup"><span data-stu-id="12540-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="12540-198">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="12540-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="12540-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="12540-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="12540-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="12540-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="12540-201">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12540-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="12540-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="12540-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="12540-203">(7)</span><span class="sxs-lookup"><span data-stu-id="12540-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="12540-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="12540-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="12540-205">(8)</span><span class="sxs-lookup"><span data-stu-id="12540-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="12540-206">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="12540-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="12540-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="12540-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="12540-208">(9)</span><span class="sxs-lookup"><span data-stu-id="12540-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="12540-209">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12540-209">Device is not working properly.</span></span> <span data-ttu-id="12540-210">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="12540-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="12540-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="12540-212">(10)</span><span class="sxs-lookup"><span data-stu-id="12540-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="12540-213">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="12540-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="12540-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="12540-215">(11)</span><span class="sxs-lookup"><span data-stu-id="12540-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="12540-216">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="12540-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="12540-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="12540-218">12</span><span class="sxs-lookup"><span data-stu-id="12540-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="12540-219">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="12540-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="12540-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="12540-221">(13)</span><span class="sxs-lookup"><span data-stu-id="12540-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="12540-222">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="12540-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="12540-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="12540-224">(14)</span><span class="sxs-lookup"><span data-stu-id="12540-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="12540-225">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="12540-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="12540-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="12540-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="12540-227">(15)</span><span class="sxs-lookup"><span data-stu-id="12540-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="12540-228">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="12540-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="12540-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="12540-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="12540-230">(16)</span><span class="sxs-lookup"><span data-stu-id="12540-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="12540-231">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="12540-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="12540-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="12540-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="12540-233">(17)</span><span class="sxs-lookup"><span data-stu-id="12540-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="12540-234">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="12540-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12540-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="12540-236">(18)</span><span class="sxs-lookup"><span data-stu-id="12540-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="12540-237">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="12540-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="12540-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="12540-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="12540-239">(19)</span><span class="sxs-lookup"><span data-stu-id="12540-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12540-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="12540-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="12540-241">(20)</span><span class="sxs-lookup"><span data-stu-id="12540-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="12540-242">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="12540-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="12540-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="12540-244">(21)</span><span class="sxs-lookup"><span data-stu-id="12540-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="12540-245">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="12540-245">System failure.</span></span> <span data-ttu-id="12540-246">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="12540-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="12540-247">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="12540-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="12540-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="12540-249">(22)</span><span class="sxs-lookup"><span data-stu-id="12540-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="12540-250">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="12540-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="12540-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="12540-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="12540-252">(23)</span><span class="sxs-lookup"><span data-stu-id="12540-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="12540-253">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="12540-253">System failure.</span></span> <span data-ttu-id="12540-254">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="12540-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="12540-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="12540-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="12540-256">(24)</span><span class="sxs-lookup"><span data-stu-id="12540-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="12540-257">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="12540-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12540-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12540-259">(25)</span><span class="sxs-lookup"><span data-stu-id="12540-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="12540-260">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12540-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12540-262">(26)</span><span class="sxs-lookup"><span data-stu-id="12540-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="12540-263">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="12540-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="12540-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="12540-265">(27)</span><span class="sxs-lookup"><span data-stu-id="12540-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="12540-266">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="12540-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="12540-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="12540-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="12540-268">(28)</span><span class="sxs-lookup"><span data-stu-id="12540-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="12540-269">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="12540-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="12540-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="12540-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="12540-271">(29)</span><span class="sxs-lookup"><span data-stu-id="12540-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="12540-272">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="12540-272">Device is disabled.</span></span> <span data-ttu-id="12540-273">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="12540-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="12540-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="12540-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="12540-275">(30)</span><span class="sxs-lookup"><span data-stu-id="12540-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="12540-276">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="12540-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12540-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12540-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="12540-278">(31)</span><span class="sxs-lookup"><span data-stu-id="12540-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="12540-279">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12540-279">Device is not working properly.</span></span> <span data-ttu-id="12540-280">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="12540-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12540-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="12540-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-282">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12540-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12540-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-284">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12540-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12540-285">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="12540-285">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="12540-286">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12540-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-290">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12540-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12540-291">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="12540-291">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="12540-292">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="12540-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="12540-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-294">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12540-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-297">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="12540-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="12540-298">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="12540-298">Description of the object.</span></span>

<span data-ttu-id="12540-299">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12540-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-300">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="12540-300">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-301">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12540-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12540-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-303">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="12540-303">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="12540-304">Velocidade do ventilador solicitada no momento, definida em rotações por minuto, quando há suporte para um ventilador de velocidade variável (**variablespeed** é **true**).</span><span class="sxs-lookup"><span data-stu-id="12540-304">Currently requested fan speed, defined in revolutions per minute, when a variable speed fan is supported (**VariableSpeed** is **TRUE**).</span></span> <span data-ttu-id="12540-305">A velocidade atual é determinada por um sensor ([**\_ tacômetro do CIM**](cim-tachometer.md)) que está associado ao ventilador usando a relação de [**\_ AssociatedSensor do CIM**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="12540-305">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="12540-306">Essa propriedade é herdada [**do \_ ventilador CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="12540-306">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

<span data-ttu-id="12540-307">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12540-307">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12540-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="12540-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-311">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="12540-311">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="12540-312">Identifica o dispositivo de ventilador.</span><span class="sxs-lookup"><span data-stu-id="12540-312">Identifies the fan device.</span></span> <span data-ttu-id="12540-313">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="12540-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-315">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12540-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12540-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-317">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="12540-317">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="12540-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="12540-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-322">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="12540-322">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="12540-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="12540-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-325">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="12540-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="12540-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-327">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="12540-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="12540-328">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="12540-328">Date and time the object was installed.</span></span> <span data-ttu-id="12540-329">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="12540-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="12540-330">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12540-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-331">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12540-331">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-332">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12540-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12540-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-334">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12540-334">Last error code reported by the logical device.</span></span>

<span data-ttu-id="12540-335">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-336">**Nome**</span><span class="sxs-lookup"><span data-stu-id="12540-336">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-339">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="12540-339">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="12540-340">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="12540-340">Label by which the object is known.</span></span> <span data-ttu-id="12540-341">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="12540-341">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="12540-342">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12540-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-343">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="12540-343">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-346">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12540-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12540-347">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12540-347">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="12540-348">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="12540-349">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="12540-349">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="12540-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="12540-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-351">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12540-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="12540-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-353">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12540-353">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="12540-354">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="12540-354">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12540-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="12540-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="12540-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="12540-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="12540-357">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12540-357">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12540-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="12540-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12540-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="12540-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="12540-360">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="12540-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="12540-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="12540-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="12540-362">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="12540-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="12540-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="12540-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="12540-364">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="12540-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="12540-365">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="12540-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="12540-366">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="12540-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="12540-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="12540-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="12540-368">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="12540-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="12540-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="12540-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="12540-370">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="12540-370">Timed Power-On Supported</span></span>

<span data-ttu-id="12540-371">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="12540-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12540-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="12540-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-373">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12540-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12540-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-375">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="12540-375">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="12540-376">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="12540-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="12540-377">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="12540-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-381">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="12540-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="12540-382">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="12540-382">Current status of the object.</span></span> <span data-ttu-id="12540-383">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="12540-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="12540-384">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="12540-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="12540-385">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="12540-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="12540-386">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="12540-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="12540-387">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="12540-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="12540-388">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12540-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="12540-389">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="12540-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="12540-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="12540-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="12540-391">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="12540-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12540-392">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="12540-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12540-393">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="12540-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="12540-394">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="12540-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="12540-395">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="12540-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="12540-396">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="12540-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="12540-397">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="12540-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="12540-398">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="12540-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="12540-399">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="12540-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="12540-400">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="12540-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="12540-401">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="12540-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12540-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="12540-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-403">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12540-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12540-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-405">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="12540-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="12540-406">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12540-406">State of the logical device.</span></span> <span data-ttu-id="12540-407">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="12540-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="12540-408">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12540-409">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="12540-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12540-410">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="12540-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12540-411">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="12540-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12540-412">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="12540-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12540-413">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="12540-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12540-414">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12540-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-417">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12540-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12540-418">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="12540-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="12540-419">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="12540-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12540-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12540-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12540-423">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12540-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12540-424">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="12540-424">Name of the scoping system.</span></span>

<span data-ttu-id="12540-425">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12540-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12540-426">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="12540-426">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12540-427">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12540-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12540-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12540-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12540-429">Se **for true**, o ventilador dará suporte a velocidades de variáveis.</span><span class="sxs-lookup"><span data-stu-id="12540-429">If **True**, the fan supports variable speeds.</span></span>

<span data-ttu-id="12540-430">Essa propriedade é herdada [**do \_ ventilador CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="12540-430">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12540-431">Comentários</span><span class="sxs-lookup"><span data-stu-id="12540-431">Remarks</span></span>

<span data-ttu-id="12540-432">A **classe \_ do ventilador do Win32** é derivada do [**\_ ventilador CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="12540-432">The **Win32\_Fan** class is derived from [**CIM\_Fan**](cim-fan.md).</span></span>

## <a name="examples"></a><span data-ttu-id="12540-433">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12540-433">Examples</span></span>

<span data-ttu-id="12540-434">A amostra do PowerShell [listar informações](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) sobre o ventilador do computador recupera informações sobre os ventiladores de resfriamento instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="12540-434">The [List Computer Fan Information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell sample retrieves information about the cooling fans installed in a computer.</span></span>

<span data-ttu-id="12540-435">O exemplo a seguir recupera informações sobre os ventiladores de resfriamento instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="12540-435">The following sample retrieves information about the cooling fans installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Fan") 
 
For Each objItem in colItems 
    Wscript.Echo "Active Cooling: " & objItem.ActiveCooling 
    Wscript.Echo "Availability: " & objItem.Availability 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
    Wscript.Echo 
Next
```


```PowerShell
$colItems = Get-WmiObject Win32_Fan -Namespace "root\cimv2"
foreach ($objItem in $colItems)
{
    "Active Cooling: " + $objItem.ActiveCooling 
    "Availability: " + $objItem.Availability 
    "Device ID: " + $objItem.DeviceID 
    "Name: " + $objItem.Name 
    "Status Information: " + $objItem.StatusInfo 
}
```





## <a name="requirements"></a><span data-ttu-id="12540-436">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12540-436">Requirements</span></span>



| <span data-ttu-id="12540-437">Requisito</span><span class="sxs-lookup"><span data-stu-id="12540-437">Requirement</span></span> | <span data-ttu-id="12540-438">Valor</span><span class="sxs-lookup"><span data-stu-id="12540-438">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12540-439">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12540-439">Minimum supported client</span></span><br/> | <span data-ttu-id="12540-440">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12540-440">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12540-441">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12540-441">Minimum supported server</span></span><br/> | <span data-ttu-id="12540-442">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12540-442">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12540-443">Namespace</span><span class="sxs-lookup"><span data-stu-id="12540-443">Namespace</span></span><br/>                | <span data-ttu-id="12540-444">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12540-444">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12540-445">MOF</span><span class="sxs-lookup"><span data-stu-id="12540-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12540-446"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12540-446"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12540-447">DLL</span><span class="sxs-lookup"><span data-stu-id="12540-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12540-448"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12540-448"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12540-449">Confira também</span><span class="sxs-lookup"><span data-stu-id="12540-449">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12540-450">**\_Ventilador CIM**</span><span class="sxs-lookup"><span data-stu-id="12540-450">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dt>

[<span data-ttu-id="12540-451">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="12540-451">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

