---
description: Epresents as propriedades de um dispositivo Plug and Play.
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088971"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="a4c5c-103">\_Classe Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="a4c5c-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="a4c5c-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PnPEntity do Win32** representa as propriedades de um dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="a4c5c-105">Plug and Play entidades são mostradas como entradas no Gerenciador de Dispositivos localizado no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="a4c5c-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a4c5c-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c5c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4c5c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a4c5c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a4c5c-109">Members</span></span>

<span data-ttu-id="a4c5c-110">A classe **Win32 \_ PnPEntity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a4c5c-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="a4c5c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4c5c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4c5c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a4c5c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4c5c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4c5c-113">Methods</span></span>

<span data-ttu-id="a4c5c-114">A classe **Win32 \_ PnPEntity** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="a4c5c-115">Método</span><span class="sxs-lookup"><span data-stu-id="a4c5c-115">Method</span></span>                                                             | <span data-ttu-id="a4c5c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4c5c-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4c5c-117">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="a4c5c-118">Desabilita este dispositivo de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="a4c5c-119">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="a4c5c-120">Habilita este dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="a4c5c-121">**Getdeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="a4c5c-122">Obtém as propriedades especificadas deste Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="a4c5c-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-123">**Reset**</span></span>                                                          | <span data-ttu-id="a4c5c-124">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-124">Not implemented.</span></span> <span data-ttu-id="a4c5c-125">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="a4c5c-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="a4c5c-127">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-127">Not implemented.</span></span> <span data-ttu-id="a4c5c-128">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a4c5c-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a4c5c-129">Properties</span></span>

<span data-ttu-id="a4c5c-130">A classe **Win32 \_ PnPEntity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4c5c-131">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-134">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-135">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-135">Availability and status of the device.</span></span>

<span data-ttu-id="a4c5c-136">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a4c5c-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a4c5c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a4c5c-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-140">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="a4c5c-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a4c5c-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a4c5c-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a4c5c-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a4c5c-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="a4c5c-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a4c5c-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a4c5c-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a4c5c-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a4c5c-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a4c5c-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a4c5c-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-151">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a4c5c-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-153">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a4c5c-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-155">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a4c5c-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a4c5c-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-158">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a4c5c-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-160">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a4c5c-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-162">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a4c5c-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-164">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a4c5c-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-166">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4c5c-167">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-170">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-171">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-171">Short description of the object.</span></span>

<span data-ttu-id="a4c5c-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-173">**ClassGuid**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-176">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-177">GUID (identificador global exclusivo) deste Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-178">**Compatívelid**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-179">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-181">Uma cadeia de caracteres de identificação definida pelo fornecedor que a instalação usa para corresponder a um dispositivo em um arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="a4c5c-182">Um dispositivo pode ter uma lista de identificações compatíveis associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="a4c5c-183">As IDs compatíveis devem ser listadas para diminuir a adequação.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="a4c5c-184">Se a instalação não puder localizar um arquivo INF que corresponda a uma das identificações de hardware de um dispositivo, ele usará IDs compatíveis para localizar um arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="a4c5c-185">Uma ID compatível tem o mesmo formato que um **HardwareID**.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="a4c5c-186">Para obter mais informações, consulte [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-188">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-190">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-191">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a4c5c-192">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a4c5c-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a4c5c-194"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-195">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a4c5c-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a4c5c-197">(1)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-198">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a4c5c-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a4c5c-200">(2)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a4c5c-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a4c5c-202">(3)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-203">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a4c5c-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a4c5c-205">(4)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-206">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-206">Device is not working properly.</span></span> <span data-ttu-id="a4c5c-207">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a4c5c-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a4c5c-209">(5)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-210">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a4c5c-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a4c5c-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-213">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a4c5c-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a4c5c-215">(7)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a4c5c-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a4c5c-217">(8)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-218">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a4c5c-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a4c5c-220">(9)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-221">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-221">Device is not working properly.</span></span> <span data-ttu-id="a4c5c-222">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a4c5c-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a4c5c-224">(10)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-225">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a4c5c-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a4c5c-227">(11)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-228">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a4c5c-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a4c5c-230">12</span><span class="sxs-lookup"><span data-stu-id="a4c5c-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-231">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a4c5c-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a4c5c-233">(13)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-234">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a4c5c-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a4c5c-236">(14)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-237">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a4c5c-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a4c5c-239">(15)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-240">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a4c5c-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a4c5c-242">(16)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-243">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a4c5c-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a4c5c-245">(17)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-246">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a4c5c-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a4c5c-248">(18)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-249">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a4c5c-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a4c5c-251">(19)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a4c5c-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a4c5c-253">(20)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-254">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a4c5c-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a4c5c-256">(21)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-257">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-257">System failure.</span></span> <span data-ttu-id="a4c5c-258">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a4c5c-259">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a4c5c-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a4c5c-261">(22)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-262">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a4c5c-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a4c5c-264">(23)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-265">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-265">System failure.</span></span> <span data-ttu-id="a4c5c-266">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a4c5c-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a4c5c-268">(24)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-269">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a4c5c-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a4c5c-271">(25)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-272">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a4c5c-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a4c5c-274">(26)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-275">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a4c5c-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a4c5c-277">(27)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-278">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a4c5c-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a4c5c-280">(28)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-281">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a4c5c-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a4c5c-283">(29)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-284">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-284">Device is disabled.</span></span> <span data-ttu-id="a4c5c-285">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a4c5c-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a4c5c-287">(30)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-288">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a4c5c-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a4c5c-290">(31)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-291">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-291">Device is not working properly.</span></span> <span data-ttu-id="a4c5c-292">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4c5c-293">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-294">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-296">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-297">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a4c5c-298">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-299">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-302">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-303">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a4c5c-304">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a4c5c-305">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-306">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-309">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-310">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-310">Description of the object.</span></span>

<span data-ttu-id="a4c5c-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-315">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-316">Identificador do dispositivo de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="a4c5c-317">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-319">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-321">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a4c5c-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-326">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="a4c5c-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-328">**HardwareID**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-329">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-331">Uma cadeia de caracteres de identificação definida pelo fornecedor que a instalação usa para corresponder a um dispositivo em um arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="a4c5c-332">Normalmente, um dispositivo tem uma lista associada de IDs de hardware.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="a4c5c-333">Uma exceção é o driver de barramento 1394, que não usa IDs de hardware.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="a4c5c-334">A primeira ID de hardware na lista deve ser a ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="a4c5c-335">As IDs restantes devem ser listadas para diminuir a adequação.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="a4c5c-336">As IDs de hardware aparecem em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="a4c5c-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="a4c5c-337">\\enumerador de enumerador-específico-Device-ID</span><span class="sxs-lookup"><span data-stu-id="a4c5c-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="a4c5c-338">Esse é o formato mais comum para dispositivos PnP individuais.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="a4c5c-339">Um exemplo de um enumerador é o BIOS ou o ISAPNP.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="a4c5c-340">\*ID específica do enumerador</span><span class="sxs-lookup"><span data-stu-id="a4c5c-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="a4c5c-341">Um asterisco ( \* ) indica uso por mais de um enumerador.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="a4c5c-342">ID específica de classe de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a4c5c-342">device-class-specific ID</span></span>

    <span data-ttu-id="a4c5c-343">Um formato personalizado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-343">A custom format.</span></span>

<span data-ttu-id="a4c5c-344">Exemplos de IDs de hardware:</span><span class="sxs-lookup"><span data-stu-id="a4c5c-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="a4c5c-345">\\ \* PNPOF08 raiz</span><span class="sxs-lookup"><span data-stu-id="a4c5c-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="a4c5c-346">PC \\ VEN \_ 1000&DEV \_ 001&subsis \_ 00000000&rev \_ 02</span><span class="sxs-lookup"><span data-stu-id="a4c5c-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="a4c5c-347">Para obter mais informações, consulte o [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-349">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-351">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-352">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-352">Date and time the object was installed.</span></span> <span data-ttu-id="a4c5c-353">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a4c5c-354">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-355">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-356">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-358">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a4c5c-359">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-360">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-363">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-364">Nome do fabricante do dispositivo de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="a4c5c-365">Exemplo: "Acme"</span><span class="sxs-lookup"><span data-stu-id="a4c5c-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-366">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-369">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-370">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-370">Label by which the object is known.</span></span> <span data-ttu-id="a4c5c-371">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a4c5c-372">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-373">**PNPClass**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-376">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="a4c5c-377">Essa propriedade, apesar de estar listada no arquivo MOF, na verdade não existe na classe.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="a4c5c-378">A propriedade é descrita aqui apenas para fins de integridade e para esclarecer o próprio arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="a4c5c-379">O nome do tipo deste Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="a4c5c-380">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Essa propriedade não está no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-384">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-385">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a4c5c-386">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a4c5c-387">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a4c5c-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-388">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-389">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-391">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-391">Not implemented.</span></span>

<span data-ttu-id="a4c5c-392">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a4c5c-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-394">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a4c5c-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-396">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a4c5c-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-398">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a4c5c-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-400">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a4c5c-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-402">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a4c5c-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-404">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="a4c5c-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="a4c5c-405">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="a4c5c-406">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a4c5c-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-408">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="a4c5c-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a4c5c-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a4c5c-410">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4c5c-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-412">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-414">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-414">Not implemented.</span></span>

<span data-ttu-id="a4c5c-415">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-416">**Presente**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-417">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-419">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-420">Se este Plug and Play dispositivo está atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="a4c5c-421">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-422">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-423">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-425">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-426">Nome do serviço que dá suporte a este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="a4c5c-427">Para obter mais informações, consulte [**Win32 \_ SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="a4c5c-428">Exemplo: "ATAPI"</span><span class="sxs-lookup"><span data-stu-id="a4c5c-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-432">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-433">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-433">Current status of the object.</span></span> <span data-ttu-id="a4c5c-434">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a4c5c-435">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a4c5c-436">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="a4c5c-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a4c5c-437">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a4c5c-438">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a4c5c-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a4c5c-440">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a4c5c-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a4c5c-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a4c5c-442">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a4c5c-443">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a4c5c-444">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a4c5c-445">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a4c5c-446">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a4c5c-447">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a4c5c-448">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a4c5c-449">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a4c5c-450">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a4c5c-451">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a4c5c-452">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a4c5c-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-456">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="a4c5c-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-457">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-457">State of the logical device.</span></span> <span data-ttu-id="a4c5c-458">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a4c5c-459">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a4c5c-460">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a4c5c-461">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a4c5c-462">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a4c5c-463">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a4c5c-464">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a4c5c-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-468">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-469">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a4c5c-470">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4c5c-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c5c-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4c5c-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c5c-474">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a4c5c-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a4c5c-475">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-475">Name of the scoping system.</span></span>

<span data-ttu-id="a4c5c-476">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4c5c-477">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4c5c-477">Remarks</span></span>

<span data-ttu-id="a4c5c-478">A classe **Win32 \_ PnPEntity** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a4c5c-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a4c5c-479">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4c5c-479">Examples</span></span>

<span data-ttu-id="a4c5c-480">A amostra do [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell na galeria do TechNet usa o **Win32 \_ PnPEntity** para recuperar uma lista de hardwares que não funciona usando o WMI.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="a4c5c-481">O exemplo de código VBScript a seguir se conecta a um grupo de computadores remotos no mesmo domínio criando uma matriz de nomes de computador remoto e, em seguida, exibindo os nomes dos dispositivos Plug and Play — instâncias do Win32 \_ PnPEntity — em cada computador.</span><span class="sxs-lookup"><span data-stu-id="a4c5c-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="a4c5c-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4c5c-482">Requirements</span></span>



| <span data-ttu-id="a4c5c-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c5c-483">Requirement</span></span> | <span data-ttu-id="a4c5c-484">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c5c-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c5c-485">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c5c-485">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c5c-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4c5c-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4c5c-487">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c5c-487">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c5c-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4c5c-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4c5c-489">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4c5c-489">Namespace</span></span><br/>                | <span data-ttu-id="a4c5c-490">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a4c5c-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4c5c-491">MOF</span><span class="sxs-lookup"><span data-stu-id="a4c5c-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4c5c-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4c5c-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4c5c-493">DLL</span><span class="sxs-lookup"><span data-stu-id="a4c5c-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4c5c-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4c5c-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c5c-495">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4c5c-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c5c-496">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a4c5c-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="a4c5c-497">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="a4c5c-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a4c5c-498">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="a4c5c-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="a4c5c-499">Tarefas do WMI: hardware do computador</span><span class="sxs-lookup"><span data-stu-id="a4c5c-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
