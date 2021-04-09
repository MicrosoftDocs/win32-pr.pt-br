---
description: A \_ classe WMI InfraredDevice do Win32 representa os recursos e o gerenciamento de um dispositivo de infravermelho.
ms.assetid: f129e7ce-4d50-44d0-877c-968f4865b781
ms.tgt_platform: multiple
title: Classe Win32_InfraredDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_InfraredDevice
- Win32_InfraredDevice.Reset
- Win32_InfraredDevice.SetPowerState
- Win32_InfraredDevice.Availability
- Win32_InfraredDevice.Caption
- Win32_InfraredDevice.ConfigManagerErrorCode
- Win32_InfraredDevice.ConfigManagerUserConfig
- Win32_InfraredDevice.CreationClassName
- Win32_InfraredDevice.Description
- Win32_InfraredDevice.DeviceID
- Win32_InfraredDevice.ErrorCleared
- Win32_InfraredDevice.ErrorDescription
- Win32_InfraredDevice.InstallDate
- Win32_InfraredDevice.LastErrorCode
- Win32_InfraredDevice.Manufacturer
- Win32_InfraredDevice.MaxNumberControlled
- Win32_InfraredDevice.Name
- Win32_InfraredDevice.PNPDeviceID
- Win32_InfraredDevice.PowerManagementCapabilities
- Win32_InfraredDevice.PowerManagementSupported
- Win32_InfraredDevice.ProtocolSupported
- Win32_InfraredDevice.Status
- Win32_InfraredDevice.StatusInfo
- Win32_InfraredDevice.SystemCreationClassName
- Win32_InfraredDevice.SystemName
- Win32_InfraredDevice.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a71946eeda3a8c304e1a6dda0ab2cc92e7b4489
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089024"
---
# <a name="win32_infrareddevice-class"></a><span data-ttu-id="4d355-103">\_Classe Win32 InfraredDevice</span><span class="sxs-lookup"><span data-stu-id="4d355-103">Win32\_InfraredDevice class</span></span>

<span data-ttu-id="4d355-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ InfraredDevice do Win32** representa os recursos e o gerenciamento de um dispositivo de infravermelho.</span><span class="sxs-lookup"><span data-stu-id="4d355-104">The **Win32\_InfraredDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management of an infrared device.</span></span>

<span data-ttu-id="4d355-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4d355-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4d355-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4d355-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d355-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d355-107">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{67F74295-BA42-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_InfraredDevice : CIM_InfraredController
{
  uint16   Availability;
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="4d355-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4d355-108">Members</span></span>

<span data-ttu-id="4d355-109">A classe **Win32 \_ InfraredDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4d355-109">The **Win32\_InfraredDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4d355-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d355-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d355-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d355-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d355-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d355-112">Methods</span></span>

<span data-ttu-id="4d355-113">A classe **Win32 \_ InfraredDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4d355-113">The **Win32\_InfraredDevice** class has these methods.</span></span>



| <span data-ttu-id="4d355-114">Método</span><span class="sxs-lookup"><span data-stu-id="4d355-114">Method</span></span>            | <span data-ttu-id="4d355-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d355-115">Description</span></span>                                                                                                                                                                                                                |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d355-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="4d355-116">**Reset**</span></span>         | <span data-ttu-id="4d355-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="4d355-117">Not implemented.</span></span> <span data-ttu-id="4d355-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ InfraredController**](cim-infraredcontroller.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="4d355-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_InfraredController**](cim-infraredcontroller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="4d355-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4d355-119">**SetPowerState**</span></span> | <span data-ttu-id="4d355-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="4d355-120">Not implemented.</span></span> <span data-ttu-id="4d355-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ InfraredController**](cim-infraredcontroller.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="4d355-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_InfraredController**](cim-infraredcontroller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4d355-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d355-122">Properties</span></span>

<span data-ttu-id="4d355-123">A classe **Win32 \_ InfraredDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4d355-123">The **Win32\_InfraredDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d355-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="4d355-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d355-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-127">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="4d355-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-128">Availability and status of the device.</span></span>

<span data-ttu-id="4d355-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d355-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d355-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d355-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="4d355-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4d355-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="4d355-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="4d355-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4d355-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="4d355-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4d355-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="4d355-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4d355-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="4d355-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4d355-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="4d355-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4d355-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="4d355-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4d355-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="4d355-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4d355-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="4d355-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4d355-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="4d355-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4d355-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="4d355-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4d355-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="4d355-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4d355-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4d355-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="4d355-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="4d355-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4d355-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="4d355-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4d355-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="4d355-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4d355-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="4d355-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="4d355-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4d355-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="4d355-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="4d355-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4d355-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="4d355-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="4d355-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4d355-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="4d355-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="4d355-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4d355-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="4d355-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="4d355-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d355-160">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="4d355-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-163">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4d355-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-164">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="4d355-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="4d355-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4d355-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d355-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-169">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4d355-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-170">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4d355-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="4d355-171">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4d355-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="4d355-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4d355-173"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="4d355-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-174">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4d355-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="4d355-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4d355-176">(1)</span><span class="sxs-lookup"><span data-stu-id="4d355-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-177">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4d355-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4d355-179">(2)</span><span class="sxs-lookup"><span data-stu-id="4d355-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4d355-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="4d355-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4d355-181">(3)</span><span class="sxs-lookup"><span data-stu-id="4d355-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-182">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="4d355-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4d355-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="4d355-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4d355-184">(4)</span><span class="sxs-lookup"><span data-stu-id="4d355-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-185">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-185">Device is not working properly.</span></span> <span data-ttu-id="4d355-186">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="4d355-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4d355-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="4d355-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4d355-188">(5)</span><span class="sxs-lookup"><span data-stu-id="4d355-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-189">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="4d355-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4d355-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="4d355-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4d355-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="4d355-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-192">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4d355-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4d355-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="4d355-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4d355-194">(7)</span><span class="sxs-lookup"><span data-stu-id="4d355-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4d355-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="4d355-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4d355-196">(8)</span><span class="sxs-lookup"><span data-stu-id="4d355-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-197">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="4d355-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4d355-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="4d355-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4d355-199">(9)</span><span class="sxs-lookup"><span data-stu-id="4d355-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-200">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-200">Device is not working properly.</span></span> <span data-ttu-id="4d355-201">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4d355-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="4d355-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4d355-203">(10)</span><span class="sxs-lookup"><span data-stu-id="4d355-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-204">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4d355-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="4d355-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4d355-206">(11)</span><span class="sxs-lookup"><span data-stu-id="4d355-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-207">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4d355-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="4d355-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4d355-209">12</span><span class="sxs-lookup"><span data-stu-id="4d355-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-210">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="4d355-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4d355-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4d355-212">(13)</span><span class="sxs-lookup"><span data-stu-id="4d355-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-213">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4d355-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="4d355-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4d355-215">(14)</span><span class="sxs-lookup"><span data-stu-id="4d355-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-216">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="4d355-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4d355-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="4d355-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4d355-218">(15)</span><span class="sxs-lookup"><span data-stu-id="4d355-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-219">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="4d355-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4d355-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="4d355-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4d355-221">(16)</span><span class="sxs-lookup"><span data-stu-id="4d355-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-222">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="4d355-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4d355-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="4d355-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4d355-224">(17)</span><span class="sxs-lookup"><span data-stu-id="4d355-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-225">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4d355-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4d355-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4d355-227">(18)</span><span class="sxs-lookup"><span data-stu-id="4d355-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-228">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="4d355-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4d355-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="4d355-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4d355-230">(19)</span><span class="sxs-lookup"><span data-stu-id="4d355-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4d355-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="4d355-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4d355-232">(20)</span><span class="sxs-lookup"><span data-stu-id="4d355-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-233">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="4d355-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4d355-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4d355-235">(21)</span><span class="sxs-lookup"><span data-stu-id="4d355-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-236">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="4d355-236">System failure.</span></span> <span data-ttu-id="4d355-237">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="4d355-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4d355-238">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4d355-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="4d355-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4d355-240">(22)</span><span class="sxs-lookup"><span data-stu-id="4d355-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-241">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4d355-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4d355-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="4d355-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4d355-243">(23)</span><span class="sxs-lookup"><span data-stu-id="4d355-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="4d355-244">System failure.</span></span> <span data-ttu-id="4d355-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="4d355-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4d355-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="4d355-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4d355-247">(24)</span><span class="sxs-lookup"><span data-stu-id="4d355-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-248">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="4d355-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4d355-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4d355-250">(25)</span><span class="sxs-lookup"><span data-stu-id="4d355-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-251">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4d355-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4d355-253">(26)</span><span class="sxs-lookup"><span data-stu-id="4d355-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-254">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4d355-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="4d355-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4d355-256">(27)</span><span class="sxs-lookup"><span data-stu-id="4d355-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-257">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="4d355-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4d355-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="4d355-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4d355-259">(28)</span><span class="sxs-lookup"><span data-stu-id="4d355-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-260">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="4d355-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4d355-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="4d355-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4d355-262">(29)</span><span class="sxs-lookup"><span data-stu-id="4d355-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-263">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4d355-263">Device is disabled.</span></span> <span data-ttu-id="4d355-264">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="4d355-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4d355-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="4d355-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4d355-266">(30)</span><span class="sxs-lookup"><span data-stu-id="4d355-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-267">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="4d355-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4d355-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4d355-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4d355-269">(31)</span><span class="sxs-lookup"><span data-stu-id="4d355-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-270">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-270">Device is not working properly.</span></span> <span data-ttu-id="4d355-271">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="4d355-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d355-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4d355-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-273">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4d355-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-275">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4d355-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-276">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4d355-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4d355-277">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4d355-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-281">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d355-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d355-282">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="4d355-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4d355-283">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="4d355-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="4d355-284">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-285">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4d355-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-288">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="4d355-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-289">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4d355-289">Description of the object.</span></span>

<span data-ttu-id="4d355-290">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4d355-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-294">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="4d355-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-295">Identificador exclusivo do dispositivo de infravermelho.</span><span class="sxs-lookup"><span data-stu-id="4d355-295">Unique identifier of the infrared device.</span></span>

<span data-ttu-id="4d355-296">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4d355-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-298">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4d355-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d355-300">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="4d355-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="4d355-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4d355-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d355-305">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="4d355-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="4d355-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4d355-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-308">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d355-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-310">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="4d355-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-311">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4d355-311">Date and time the object was installed.</span></span> <span data-ttu-id="4d355-312">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="4d355-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4d355-313">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4d355-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-315">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d355-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d355-317">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d355-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4d355-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-319">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="4d355-319">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-322">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="4d355-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-323">Fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-323">Manufacturer of the device.</span></span>

</dd> <dt>

<span data-ttu-id="4d355-324">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="4d355-324">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-325">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d355-325">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-327">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="4d355-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-328">Número máximo de entidades diretamente endereçáveis com suporte por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d355-328">Maximum number of directly addressable entities supportable by this device.</span></span> <span data-ttu-id="4d355-329">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4d355-329">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="4d355-330">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-330">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-331">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4d355-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-334">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4d355-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-335">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="4d355-335">Label by which the object is known.</span></span> <span data-ttu-id="4d355-336">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="4d355-336">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="4d355-337">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-338">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4d355-338">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-341">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4d355-341">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-342">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d355-342">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4d355-343">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4d355-344">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4d355-344">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4d355-345">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4d355-345">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-346">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d355-346">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4d355-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d355-348">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d355-348">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4d355-349">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="4d355-349">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d355-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4d355-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4d355-351"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="4d355-351"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4d355-352"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="4d355-352"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4d355-353"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="4d355-353"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-354">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4d355-354">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4d355-355"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="4d355-355"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-356">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="4d355-356">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4d355-357"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="4d355-357"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-358">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="4d355-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4d355-359">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="4d355-359">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4d355-360">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4d355-360">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4d355-361"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="4d355-361"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-362">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="4d355-362">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4d355-363"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="4d355-363"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4d355-364">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="4d355-364">Timed Power-On Supported</span></span>

<span data-ttu-id="4d355-365">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="4d355-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d355-366">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4d355-366">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-367">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4d355-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d355-369">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="4d355-369">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="4d355-370">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="4d355-370">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="4d355-371">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-371">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="4d355-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-373">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d355-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-375">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="4d355-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-376">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="4d355-376">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="4d355-377">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-377">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="4d355-378">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="4d355-378">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d355-379">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d355-379">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d355-380">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="4d355-380">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="4d355-381">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="4d355-381">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="4d355-382">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="4d355-382">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="4d355-383">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="4d355-383">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="4d355-384">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="4d355-384">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="4d355-385">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="4d355-385">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="4d355-386">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="4d355-386">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="4d355-387">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="4d355-387">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="4d355-388">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="4d355-388">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="4d355-389">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="4d355-389">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="4d355-390">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="4d355-390">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="4d355-391">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="4d355-391">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="4d355-392">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="4d355-392">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="4d355-393">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="4d355-393">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="4d355-394">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="4d355-394">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="4d355-395">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="4d355-395">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="4d355-396">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="4d355-396">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="4d355-397">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="4d355-397">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="4d355-398">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="4d355-398">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="4d355-399">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="4d355-399">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="4d355-400">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="4d355-400">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="4d355-401">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="4d355-401">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="4d355-402">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="4d355-402">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="4d355-403">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="4d355-403">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="4d355-404">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="4d355-404">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="4d355-405">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="4d355-405">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="4d355-406">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="4d355-406">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="4d355-407">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="4d355-407">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="4d355-408">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="4d355-408">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="4d355-409">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="4d355-409">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="4d355-410">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="4d355-410">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="4d355-411">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="4d355-411">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="4d355-412">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="4d355-412">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="4d355-413">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="4d355-413">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="4d355-414">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="4d355-414">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="4d355-415">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="4d355-415">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="4d355-416">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="4d355-416">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="4d355-417">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="4d355-417">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="4d355-418">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="4d355-418">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="4d355-419">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="4d355-419">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="4d355-420">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="4d355-420">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="4d355-421">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="4d355-421">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="4d355-422">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="4d355-422">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="4d355-423">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="4d355-423">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="4d355-424">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="4d355-424">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="4d355-425">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="4d355-425">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d355-426">**Status**</span><span class="sxs-lookup"><span data-stu-id="4d355-426">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-429">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4d355-429">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-430">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="4d355-430">Current status of the object.</span></span> <span data-ttu-id="4d355-431">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="4d355-431">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4d355-432">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="4d355-432">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4d355-433">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="4d355-433">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4d355-434">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="4d355-434">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4d355-435">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="4d355-435">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4d355-436">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-436">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4d355-437">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4d355-437">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4d355-438">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4d355-438">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4d355-439">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="4d355-439">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4d355-440">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="4d355-440">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d355-441">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="4d355-441">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4d355-442">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4d355-442">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4d355-443">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="4d355-443">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4d355-444">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="4d355-444">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4d355-445">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="4d355-445">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4d355-446">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="4d355-446">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4d355-447">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="4d355-447">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4d355-448">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="4d355-448">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4d355-449">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="4d355-449">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d355-450">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4d355-450">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-451">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d355-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-453">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="4d355-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4d355-454">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d355-454">State of the logical device.</span></span> <span data-ttu-id="4d355-455">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="4d355-455">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4d355-456">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d355-457">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d355-457">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d355-458">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="4d355-458">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4d355-459">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="4d355-459">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4d355-460">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="4d355-460">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4d355-461">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="4d355-461">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d355-462">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4d355-462">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-465">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d355-465">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d355-466">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="4d355-466">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="4d355-467">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-468">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4d355-468">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d355-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d355-471">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d355-471">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d355-472">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="4d355-472">Name of the scoping system.</span></span>

<span data-ttu-id="4d355-473">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d355-474">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="4d355-474">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d355-475">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d355-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d355-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d355-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d355-477">Data e hora da última redefinição do controlador.</span><span class="sxs-lookup"><span data-stu-id="4d355-477">Date and time the controller was last reset.</span></span> <span data-ttu-id="4d355-478">Isso pode significar que o controlador estava desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="4d355-478">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="4d355-479">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-479">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d355-480">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d355-480">Remarks</span></span>

<span data-ttu-id="4d355-481">A classe **Win32 \_ InfraredDevice** é derivada de [**CIM \_ InfraredController**](cim-infraredcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="4d355-481">The **Win32\_InfraredDevice** class is derived from [**CIM\_InfraredController**](cim-infraredcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d355-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d355-482">Requirements</span></span>



| <span data-ttu-id="4d355-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d355-483">Requirement</span></span> | <span data-ttu-id="4d355-484">Valor</span><span class="sxs-lookup"><span data-stu-id="4d355-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d355-485">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d355-485">Minimum supported client</span></span><br/> | <span data-ttu-id="4d355-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d355-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d355-487">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d355-487">Minimum supported server</span></span><br/> | <span data-ttu-id="4d355-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d355-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d355-489">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d355-489">Namespace</span></span><br/>                | <span data-ttu-id="4d355-490">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4d355-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d355-491">MOF</span><span class="sxs-lookup"><span data-stu-id="4d355-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d355-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d355-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d355-493">DLL</span><span class="sxs-lookup"><span data-stu-id="4d355-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d355-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d355-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d355-495">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d355-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d355-496">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="4d355-496">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="4d355-497">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="4d355-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

