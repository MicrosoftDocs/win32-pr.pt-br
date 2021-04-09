---
description: Representa as propriedades de um dispositivo de som em um sistema de computador que executa o Windows.
ms.assetid: 5471ffe9-60a3-466f-a608-e6268ba73c2b
ms.tgt_platform: multiple
title: Classe Win32_SoundDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SoundDevice
- Win32_SoundDevice.Reset
- Win32_SoundDevice.SetPowerState
- Win32_SoundDevice.Availability
- Win32_SoundDevice.Caption
- Win32_SoundDevice.ConfigManagerErrorCode
- Win32_SoundDevice.ConfigManagerUserConfig
- Win32_SoundDevice.CreationClassName
- Win32_SoundDevice.Description
- Win32_SoundDevice.DeviceID
- Win32_SoundDevice.DMABufferSize
- Win32_SoundDevice.ErrorCleared
- Win32_SoundDevice.ErrorDescription
- Win32_SoundDevice.InstallDate
- Win32_SoundDevice.LastErrorCode
- Win32_SoundDevice.Manufacturer
- Win32_SoundDevice.MPU401Address
- Win32_SoundDevice.Name
- Win32_SoundDevice.PNPDeviceID
- Win32_SoundDevice.PowerManagementCapabilities
- Win32_SoundDevice.PowerManagementSupported
- Win32_SoundDevice.ProductName
- Win32_SoundDevice.Status
- Win32_SoundDevice.StatusInfo
- Win32_SoundDevice.SystemCreationClassName
- Win32_SoundDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73e0ef7cbc71872d26f75311b6d72ac48bbfae8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089596"
---
# <a name="win32_sounddevice-class"></a><span data-ttu-id="380b0-103">\_Classe Win32 SoundDevice</span><span class="sxs-lookup"><span data-stu-id="380b0-103">Win32\_SoundDevice class</span></span>

<span data-ttu-id="380b0-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SoundDevice do Win32** representa as propriedades de um dispositivo de som em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="380b0-104">The **Win32\_SoundDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a sound device on a computer system running Windows.</span></span>

<span data-ttu-id="380b0-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="380b0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="380b0-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="380b0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="380b0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="380b0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SoundDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DMABufferSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MPU401Address;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="380b0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="380b0-108">Members</span></span>

<span data-ttu-id="380b0-109">A classe **Win32 \_ SoundDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="380b0-109">The **Win32\_SoundDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="380b0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="380b0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="380b0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="380b0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="380b0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="380b0-112">Methods</span></span>

<span data-ttu-id="380b0-113">A classe **Win32 \_ SoundDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="380b0-113">The **Win32\_SoundDevice** class has these methods.</span></span>



| <span data-ttu-id="380b0-114">Método</span><span class="sxs-lookup"><span data-stu-id="380b0-114">Method</span></span>            | <span data-ttu-id="380b0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="380b0-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380b0-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="380b0-116">**Reset**</span></span>         | <span data-ttu-id="380b0-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="380b0-117">Not implemented.</span></span> <span data-ttu-id="380b0-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="380b0-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="380b0-119">**SetPowerState**</span></span> | <span data-ttu-id="380b0-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="380b0-120">Not implemented.</span></span> <span data-ttu-id="380b0-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="380b0-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="380b0-122">Properties</span></span>

<span data-ttu-id="380b0-123">A classe **Win32 \_ SoundDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="380b0-123">The **Win32\_SoundDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="380b0-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="380b0-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="380b0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="380b0-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-128">Availability and status of the device.</span></span>

<span data-ttu-id="380b0-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="380b0-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="380b0-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="380b0-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="380b0-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="380b0-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="380b0-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="380b0-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="380b0-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="380b0-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="380b0-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="380b0-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="380b0-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="380b0-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="380b0-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="380b0-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="380b0-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="380b0-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="380b0-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="380b0-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="380b0-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="380b0-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="380b0-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="380b0-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="380b0-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="380b0-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="380b0-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="380b0-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="380b0-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="380b0-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="380b0-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="380b0-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="380b0-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="380b0-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="380b0-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="380b0-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="380b0-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="380b0-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="380b0-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="380b0-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="380b0-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="380b0-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="380b0-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="380b0-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="380b0-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="380b0-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="380b0-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="380b0-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="380b0-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="380b0-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="380b0-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="380b0-160">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="380b0-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-163">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="380b0-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-164">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="380b0-164">Short description of the object.</span></span>

<span data-ttu-id="380b0-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="380b0-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="380b0-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-169">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="380b0-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-170">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="380b0-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="380b0-171">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="380b0-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="380b0-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="380b0-173"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="380b0-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-174">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="380b0-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="380b0-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="380b0-176">(1)</span><span class="sxs-lookup"><span data-stu-id="380b0-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-177">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="380b0-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="380b0-179">(2)</span><span class="sxs-lookup"><span data-stu-id="380b0-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="380b0-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="380b0-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="380b0-181">(3)</span><span class="sxs-lookup"><span data-stu-id="380b0-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-182">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="380b0-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="380b0-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="380b0-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="380b0-184">(4)</span><span class="sxs-lookup"><span data-stu-id="380b0-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-185">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-185">Device is not working properly.</span></span> <span data-ttu-id="380b0-186">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="380b0-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="380b0-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="380b0-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="380b0-188">(5)</span><span class="sxs-lookup"><span data-stu-id="380b0-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-189">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="380b0-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="380b0-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="380b0-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="380b0-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="380b0-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-192">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="380b0-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="380b0-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="380b0-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="380b0-194">(7)</span><span class="sxs-lookup"><span data-stu-id="380b0-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="380b0-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="380b0-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="380b0-196">(8)</span><span class="sxs-lookup"><span data-stu-id="380b0-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-197">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="380b0-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="380b0-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="380b0-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="380b0-199">(9)</span><span class="sxs-lookup"><span data-stu-id="380b0-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-200">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-200">Device is not working properly.</span></span> <span data-ttu-id="380b0-201">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="380b0-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="380b0-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="380b0-203">(10)</span><span class="sxs-lookup"><span data-stu-id="380b0-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-204">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="380b0-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="380b0-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="380b0-206">(11)</span><span class="sxs-lookup"><span data-stu-id="380b0-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-207">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="380b0-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="380b0-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="380b0-209">12</span><span class="sxs-lookup"><span data-stu-id="380b0-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-210">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="380b0-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="380b0-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="380b0-212">(13)</span><span class="sxs-lookup"><span data-stu-id="380b0-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-213">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="380b0-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="380b0-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="380b0-215">(14)</span><span class="sxs-lookup"><span data-stu-id="380b0-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-216">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="380b0-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="380b0-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="380b0-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="380b0-218">(15)</span><span class="sxs-lookup"><span data-stu-id="380b0-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-219">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="380b0-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="380b0-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="380b0-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="380b0-221">(16)</span><span class="sxs-lookup"><span data-stu-id="380b0-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-222">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="380b0-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="380b0-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="380b0-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="380b0-224">(17)</span><span class="sxs-lookup"><span data-stu-id="380b0-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-225">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="380b0-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="380b0-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="380b0-227">(18)</span><span class="sxs-lookup"><span data-stu-id="380b0-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-228">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="380b0-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="380b0-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="380b0-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="380b0-230">(19)</span><span class="sxs-lookup"><span data-stu-id="380b0-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="380b0-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="380b0-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="380b0-232">(20)</span><span class="sxs-lookup"><span data-stu-id="380b0-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-233">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="380b0-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="380b0-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="380b0-235">(21)</span><span class="sxs-lookup"><span data-stu-id="380b0-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-236">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="380b0-236">System failure.</span></span> <span data-ttu-id="380b0-237">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="380b0-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="380b0-238">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="380b0-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="380b0-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="380b0-240">(22)</span><span class="sxs-lookup"><span data-stu-id="380b0-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-241">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="380b0-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="380b0-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="380b0-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="380b0-243">(23)</span><span class="sxs-lookup"><span data-stu-id="380b0-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="380b0-244">System failure.</span></span> <span data-ttu-id="380b0-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="380b0-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="380b0-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="380b0-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="380b0-247">(24)</span><span class="sxs-lookup"><span data-stu-id="380b0-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-248">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="380b0-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="380b0-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="380b0-250">(25)</span><span class="sxs-lookup"><span data-stu-id="380b0-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-251">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="380b0-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="380b0-253">(26)</span><span class="sxs-lookup"><span data-stu-id="380b0-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-254">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380b0-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="380b0-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="380b0-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="380b0-256">(27)</span><span class="sxs-lookup"><span data-stu-id="380b0-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-257">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="380b0-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="380b0-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="380b0-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="380b0-259">(28)</span><span class="sxs-lookup"><span data-stu-id="380b0-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-260">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="380b0-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="380b0-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="380b0-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="380b0-262">(29)</span><span class="sxs-lookup"><span data-stu-id="380b0-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-263">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="380b0-263">Device is disabled.</span></span> <span data-ttu-id="380b0-264">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="380b0-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="380b0-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="380b0-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="380b0-266">(30)</span><span class="sxs-lookup"><span data-stu-id="380b0-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-267">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="380b0-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="380b0-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="380b0-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="380b0-269">(31)</span><span class="sxs-lookup"><span data-stu-id="380b0-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-270">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-270">Device is not working properly.</span></span> <span data-ttu-id="380b0-271">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="380b0-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="380b0-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="380b0-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-273">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="380b0-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-275">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="380b0-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-276">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="380b0-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="380b0-277">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="380b0-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-281">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="380b0-281">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="380b0-282">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="380b0-282">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="380b0-283">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="380b0-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="380b0-284">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-285">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="380b0-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-288">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="380b0-288">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-289">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="380b0-289">Description of the object.</span></span>

<span data-ttu-id="380b0-290">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="380b0-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-294">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ MediaResources \\ \\ Wave \| DeviceID")</span><span class="sxs-lookup"><span data-stu-id="380b0-294">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\wave\|DeviceID")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-295">Identificador exclusivo do dispositivo de som.</span><span class="sxs-lookup"><span data-stu-id="380b0-295">Unique identifier of the sound device.</span></span>

<span data-ttu-id="380b0-296">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-297">**DMABufferSize**</span><span class="sxs-lookup"><span data-stu-id="380b0-297">**DMABufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-298">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="380b0-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-300">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="380b0-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-301">Tamanho do buffer de acesso direto à memória.</span><span class="sxs-lookup"><span data-stu-id="380b0-301">Size of the Direct Memory Access buffer.</span></span>

<span data-ttu-id="380b0-302">Exemplo: 4</span><span class="sxs-lookup"><span data-stu-id="380b0-302">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="380b0-303">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="380b0-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-304">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="380b0-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="380b0-306">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="380b0-306">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="380b0-307">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="380b0-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="380b0-311">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="380b0-311">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="380b0-312">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="380b0-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-314">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="380b0-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-316">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="380b0-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-317">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="380b0-317">Date and time the object was installed.</span></span> <span data-ttu-id="380b0-318">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="380b0-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="380b0-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="380b0-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-321">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="380b0-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="380b0-323">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="380b0-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="380b0-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-325">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="380b0-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-328">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="380b0-328">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-329">Fabricante do dispositivo de som.</span><span class="sxs-lookup"><span data-stu-id="380b0-329">Manufacturer of the sound device.</span></span>

<span data-ttu-id="380b0-330">Exemplo: "Creative Labs"</span><span class="sxs-lookup"><span data-stu-id="380b0-330">Example: "Creative Labs"</span></span>

</dd> <dt>

<span data-ttu-id="380b0-331">**Endereço MPU401**</span><span class="sxs-lookup"><span data-stu-id="380b0-331">**MPU401Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-332">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="380b0-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-334">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="380b0-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-335">Iniciando o endereço de e/s atribuído à porta MPU-401 do dispositivo de som.</span><span class="sxs-lookup"><span data-stu-id="380b0-335">Starting I/O address assigned to the MPU-401 port of the sound device.</span></span>

<span data-ttu-id="380b0-336">Exemplo: 300</span><span class="sxs-lookup"><span data-stu-id="380b0-336">Example: 300</span></span>

</dd> <dt>

<span data-ttu-id="380b0-337">**Nome**</span><span class="sxs-lookup"><span data-stu-id="380b0-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-340">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="380b0-340">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-341">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="380b0-341">Label by which the object is known.</span></span> <span data-ttu-id="380b0-342">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="380b0-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="380b0-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="380b0-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-347">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="380b0-347">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-348">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="380b0-348">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="380b0-349">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="380b0-350">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="380b0-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="380b0-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="380b0-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-352">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="380b0-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="380b0-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="380b0-354">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="380b0-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="380b0-355">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="380b0-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="380b0-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="380b0-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="380b0-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="380b0-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="380b0-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="380b0-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="380b0-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="380b0-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-360">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="380b0-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="380b0-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="380b0-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-362">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="380b0-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="380b0-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="380b0-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-364">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="380b0-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="380b0-365">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="380b0-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="380b0-366">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-366">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="380b0-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="380b0-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-368">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="380b0-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="380b0-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="380b0-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="380b0-370">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="380b0-370">Timed Power-On Supported</span></span>

<span data-ttu-id="380b0-371">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="380b0-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="380b0-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="380b0-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-373">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="380b0-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="380b0-375">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="380b0-375">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="380b0-376">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="380b0-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="380b0-377">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-378">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="380b0-378">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-381">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de multimídia win32api \| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) \| szPname")</span><span class="sxs-lookup"><span data-stu-id="380b0-381">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Multimedia Structures\|[**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)\|szPname")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-382">Nome do produto do dispositivo de som.</span><span class="sxs-lookup"><span data-stu-id="380b0-382">Product name of the sound device.</span></span>

<span data-ttu-id="380b0-383">Exemplo: "Creative Labs SoundBlaster AWE64PNP"</span><span class="sxs-lookup"><span data-stu-id="380b0-383">Example: "Creative Labs SoundBlaster AWE64PNP"</span></span>

</dd> <dt>

<span data-ttu-id="380b0-384">**Status**</span><span class="sxs-lookup"><span data-stu-id="380b0-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-387">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="380b0-387">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-388">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="380b0-388">Current status of the object.</span></span> <span data-ttu-id="380b0-389">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="380b0-389">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="380b0-390">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="380b0-390">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="380b0-391">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="380b0-391">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="380b0-392">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="380b0-392">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="380b0-393">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="380b0-393">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="380b0-394">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-394">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="380b0-395">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="380b0-395">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="380b0-396">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="380b0-396">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="380b0-397">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="380b0-397">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="380b0-398">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="380b0-398">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="380b0-399">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="380b0-399">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="380b0-400">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="380b0-400">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="380b0-401">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="380b0-401">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="380b0-402">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="380b0-402">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="380b0-403">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="380b0-403">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="380b0-404">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="380b0-404">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="380b0-405">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="380b0-405">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="380b0-406">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="380b0-406">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="380b0-407">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="380b0-407">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="380b0-408">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="380b0-408">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-409">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="380b0-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-411">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="380b0-411">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="380b0-412">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="380b0-412">State of the logical device.</span></span> <span data-ttu-id="380b0-413">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="380b0-413">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="380b0-414">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="380b0-415">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="380b0-415">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="380b0-416">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="380b0-416">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="380b0-417">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="380b0-417">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="380b0-418">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="380b0-418">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="380b0-419">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="380b0-419">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="380b0-420">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="380b0-420">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-423">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="380b0-423">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="380b0-424">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="380b0-424">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="380b0-425">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="380b0-426">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="380b0-426">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="380b0-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="380b0-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="380b0-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="380b0-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="380b0-429">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="380b0-429">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="380b0-430">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="380b0-430">Name of the scoping system.</span></span>

<span data-ttu-id="380b0-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="380b0-432">Comentários</span><span class="sxs-lookup"><span data-stu-id="380b0-432">Remarks</span></span>

<span data-ttu-id="380b0-433">A classe **Win32 \_ SoundDevice** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="380b0-433">The **Win32\_SoundDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="380b0-434">Exemplos</span><span class="sxs-lookup"><span data-stu-id="380b0-434">Examples</span></span>

<span data-ttu-id="380b0-435">A amostra do PowerShell [listar Propriedades da placa de som](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) recupera informações sobre todas as placas de som instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="380b0-435">The [List Sound Card Properties](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) PowerShell sample retrieves information about all the sound cards installed in a computer.</span></span>

<span data-ttu-id="380b0-436">O exemplo de VBScript a seguir recupera informações sobre todas as placas de som instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="380b0-436">The following VBScript sample retrieves information about all the sound cards installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SoundDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "DMA Buffer Size: " & objItem.DMABufferSize 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "MPU 401 Address: " & objItem.MPU401Address 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Product Name: " & objItem.ProductName 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="380b0-437">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380b0-437">Requirements</span></span>



| <span data-ttu-id="380b0-438">Requisito</span><span class="sxs-lookup"><span data-stu-id="380b0-438">Requirement</span></span> | <span data-ttu-id="380b0-439">Valor</span><span class="sxs-lookup"><span data-stu-id="380b0-439">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="380b0-440">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="380b0-440">Minimum supported client</span></span><br/> | <span data-ttu-id="380b0-441">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="380b0-441">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="380b0-442">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="380b0-442">Minimum supported server</span></span><br/> | <span data-ttu-id="380b0-443">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="380b0-443">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="380b0-444">Namespace</span><span class="sxs-lookup"><span data-stu-id="380b0-444">Namespace</span></span><br/>                | <span data-ttu-id="380b0-445">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="380b0-445">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="380b0-446">MOF</span><span class="sxs-lookup"><span data-stu-id="380b0-446">MOF</span></span><br/>                      | <dl> <span data-ttu-id="380b0-447"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="380b0-447"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="380b0-448">DLL</span><span class="sxs-lookup"><span data-stu-id="380b0-448">DLL</span></span><br/>                      | <dl> <span data-ttu-id="380b0-449"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="380b0-449"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="380b0-450">Confira também</span><span class="sxs-lookup"><span data-stu-id="380b0-450">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380b0-451">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="380b0-451">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="380b0-452">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="380b0-452">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
