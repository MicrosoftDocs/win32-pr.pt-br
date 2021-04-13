---
description: Representa o tipo de monitor ou dispositivo de exibição conectado ao sistema de computador.
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Classe Win32_DesktopMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501110"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="c33f6-103">\_Classe Win32 DesktopMonitor</span><span class="sxs-lookup"><span data-stu-id="c33f6-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="c33f6-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DesktopMonitor do Win32** representa o tipo de monitor ou dispositivo de vídeo anexado ao sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="c33f6-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="c33f6-105">O hardware que não é compatível com o Windows Display Driver Model (WDDM) retorna valores de propriedade imprecisos para instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c33f6-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="c33f6-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c33f6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c33f6-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c33f6-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33f6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c33f6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="c33f6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c33f6-109">Members</span></span>

<span data-ttu-id="c33f6-110">A classe **Win32 \_ DesktopMonitor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c33f6-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="c33f6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c33f6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c33f6-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c33f6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c33f6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c33f6-113">Methods</span></span>

<span data-ttu-id="c33f6-114">A classe **Win32 \_ DesktopMonitor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c33f6-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="c33f6-115">Método</span><span class="sxs-lookup"><span data-stu-id="c33f6-115">Method</span></span>            | <span data-ttu-id="c33f6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c33f6-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33f6-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c33f6-117">**Reset**</span></span>         | <span data-ttu-id="c33f6-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-118">Not implemented.</span></span> <span data-ttu-id="c33f6-119">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="c33f6-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="c33f6-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c33f6-120">**SetPowerState**</span></span> | <span data-ttu-id="c33f6-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-121">Not implemented.</span></span> <span data-ttu-id="c33f6-122">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="c33f6-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c33f6-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c33f6-123">Properties</span></span>

<span data-ttu-id="c33f6-124">A classe **Win32 \_ DesktopMonitor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c33f6-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c33f6-125">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="c33f6-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c33f6-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c33f6-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-129">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-129">Availability and status of the device.</span></span>

<span data-ttu-id="c33f6-130">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c33f6-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c33f6-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c33f6-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c33f6-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c33f6-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c33f6-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-134">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="c33f6-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c33f6-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="c33f6-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c33f6-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="c33f6-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c33f6-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="c33f6-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c33f6-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="c33f6-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c33f6-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="c33f6-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c33f6-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="c33f6-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c33f6-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c33f6-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c33f6-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c33f6-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c33f6-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="c33f6-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c33f6-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="c33f6-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c33f6-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c33f6-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="c33f6-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c33f6-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c33f6-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c33f6-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="c33f6-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c33f6-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="c33f6-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c33f6-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c33f6-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c33f6-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c33f6-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c33f6-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="c33f6-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="c33f6-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c33f6-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c33f6-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c33f6-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="c33f6-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="c33f6-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c33f6-161">**Largura de banda**</span><span class="sxs-lookup"><span data-stu-id="c33f6-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-164">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="c33f6-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-165">Largura de banda do monitor em megahertz.</span><span class="sxs-lookup"><span data-stu-id="c33f6-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="c33f6-166">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c33f6-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="c33f6-167">Essa propriedade é herdada do [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-168">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c33f6-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-171">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c33f6-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-172">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c33f6-172">Short description of the object.</span></span>

<span data-ttu-id="c33f6-173">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c33f6-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-175">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-177">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c33f6-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-178">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c33f6-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c33f6-179">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c33f6-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c33f6-181"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="c33f6-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-182">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c33f6-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c33f6-184">(1)</span><span class="sxs-lookup"><span data-stu-id="c33f6-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-185">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c33f6-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c33f6-187">(2)</span><span class="sxs-lookup"><span data-stu-id="c33f6-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c33f6-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c33f6-189">(3)</span><span class="sxs-lookup"><span data-stu-id="c33f6-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-190">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="c33f6-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c33f6-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c33f6-192">(4)</span><span class="sxs-lookup"><span data-stu-id="c33f6-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-193">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-193">Device is not working properly.</span></span> <span data-ttu-id="c33f6-194">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c33f6-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c33f6-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c33f6-196">(5)</span><span class="sxs-lookup"><span data-stu-id="c33f6-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-197">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="c33f6-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c33f6-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c33f6-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="c33f6-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-200">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c33f6-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c33f6-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c33f6-202">(7)</span><span class="sxs-lookup"><span data-stu-id="c33f6-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c33f6-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c33f6-204">(8)</span><span class="sxs-lookup"><span data-stu-id="c33f6-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-205">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c33f6-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c33f6-207">(9)</span><span class="sxs-lookup"><span data-stu-id="c33f6-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-208">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-208">Device is not working properly.</span></span> <span data-ttu-id="c33f6-209">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c33f6-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c33f6-211">(10)</span><span class="sxs-lookup"><span data-stu-id="c33f6-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-212">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c33f6-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c33f6-214">(11)</span><span class="sxs-lookup"><span data-stu-id="c33f6-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-215">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c33f6-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c33f6-217">12</span><span class="sxs-lookup"><span data-stu-id="c33f6-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-218">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="c33f6-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c33f6-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c33f6-220">(13)</span><span class="sxs-lookup"><span data-stu-id="c33f6-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-221">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c33f6-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c33f6-223">(14)</span><span class="sxs-lookup"><span data-stu-id="c33f6-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-224">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c33f6-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c33f6-226">(15)</span><span class="sxs-lookup"><span data-stu-id="c33f6-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-227">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="c33f6-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c33f6-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c33f6-229">(16)</span><span class="sxs-lookup"><span data-stu-id="c33f6-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-230">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="c33f6-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c33f6-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c33f6-232">(17)</span><span class="sxs-lookup"><span data-stu-id="c33f6-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-233">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c33f6-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c33f6-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c33f6-235">(18)</span><span class="sxs-lookup"><span data-stu-id="c33f6-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-236">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="c33f6-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c33f6-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c33f6-238">(19)</span><span class="sxs-lookup"><span data-stu-id="c33f6-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c33f6-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c33f6-240">(20)</span><span class="sxs-lookup"><span data-stu-id="c33f6-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-241">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c33f6-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c33f6-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c33f6-243">(21)</span><span class="sxs-lookup"><span data-stu-id="c33f6-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c33f6-244">System failure.</span></span> <span data-ttu-id="c33f6-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c33f6-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c33f6-246">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c33f6-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c33f6-248">(22)</span><span class="sxs-lookup"><span data-stu-id="c33f6-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-249">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c33f6-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c33f6-251">(23)</span><span class="sxs-lookup"><span data-stu-id="c33f6-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-252">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c33f6-252">System failure.</span></span> <span data-ttu-id="c33f6-253">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c33f6-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c33f6-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c33f6-255">(24)</span><span class="sxs-lookup"><span data-stu-id="c33f6-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-256">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="c33f6-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c33f6-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c33f6-258">(25)</span><span class="sxs-lookup"><span data-stu-id="c33f6-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c33f6-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c33f6-261">(26)</span><span class="sxs-lookup"><span data-stu-id="c33f6-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-262">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c33f6-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c33f6-264">(27)</span><span class="sxs-lookup"><span data-stu-id="c33f6-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-265">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="c33f6-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c33f6-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c33f6-267">(28)</span><span class="sxs-lookup"><span data-stu-id="c33f6-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-268">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="c33f6-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c33f6-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c33f6-270">(29)</span><span class="sxs-lookup"><span data-stu-id="c33f6-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-271">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-271">Device is disabled.</span></span> <span data-ttu-id="c33f6-272">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="c33f6-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c33f6-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c33f6-274">(30)</span><span class="sxs-lookup"><span data-stu-id="c33f6-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-275">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="c33f6-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c33f6-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c33f6-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c33f6-277">(31)</span><span class="sxs-lookup"><span data-stu-id="c33f6-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-278">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-278">Device is not working properly.</span></span> <span data-ttu-id="c33f6-279">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="c33f6-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c33f6-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c33f6-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-281">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c33f6-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-283">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c33f6-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-284">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c33f6-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c33f6-285">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c33f6-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-289">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c33f6-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-290">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c33f6-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c33f6-291">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c33f6-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c33f6-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-293">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c33f6-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-296">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c33f6-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-297">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c33f6-297">Description of the object.</span></span>

<span data-ttu-id="c33f6-298">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-299">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c33f6-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-302">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GDI Windows \| HMONITOR")</span><span class="sxs-lookup"><span data-stu-id="c33f6-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-303">Identificador exclusivo de um monitor de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c33f6-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="c33f6-304">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-305">**TipoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="c33f6-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-306">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c33f6-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-308">Tipo de monitor de área de trabalho ou CRT.</span><span class="sxs-lookup"><span data-stu-id="c33f6-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="c33f6-309">Essa propriedade é herdada do [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c33f6-310">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c33f6-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c33f6-311">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c33f6-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="c33f6-312">**Cor de MultiScan** (2)</span><span class="sxs-lookup"><span data-stu-id="c33f6-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="c33f6-313">**Multiexame monocromático** (3)</span><span class="sxs-lookup"><span data-stu-id="c33f6-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="c33f6-314">**Cor de frequência fixa** (4)</span><span class="sxs-lookup"><span data-stu-id="c33f6-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="c33f6-315">**Frequência fixa monocromático** (5)</span><span class="sxs-lookup"><span data-stu-id="c33f6-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c33f6-316">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c33f6-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-317">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c33f6-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-319">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c33f6-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c33f6-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-324">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="c33f6-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="c33f6-325">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c33f6-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-327">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c33f6-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-329">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c33f6-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-330">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-330">Date and time the object was installed.</span></span> <span data-ttu-id="c33f6-331">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c33f6-332">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="c33f6-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-334">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c33f6-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-336">Se for **true**, o dispositivo será bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="c33f6-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="c33f6-337">Essa propriedade é herdada [**do \_ userdevice do CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-338">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c33f6-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-339">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-341">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c33f6-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c33f6-342">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-343">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="c33f6-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-346">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="c33f6-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-347">Nome do fabricante do monitor.</span><span class="sxs-lookup"><span data-stu-id="c33f6-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="c33f6-348">Exemplo: "NEC"</span><span class="sxs-lookup"><span data-stu-id="c33f6-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-349">**Monitor**</span><span class="sxs-lookup"><span data-stu-id="c33f6-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-352">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="c33f6-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-353">Tipo de monitor.</span><span class="sxs-lookup"><span data-stu-id="c33f6-353">Type of monitor.</span></span>

<span data-ttu-id="c33f6-354">Exemplo: "NEC 5FGp"</span><span class="sxs-lookup"><span data-stu-id="c33f6-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-355">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c33f6-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-358">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c33f6-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-359">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c33f6-359">Label by which the object is known.</span></span> <span data-ttu-id="c33f6-360">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c33f6-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c33f6-361">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-362">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="c33f6-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-363">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-365">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels por polegada lógica")</span><span class="sxs-lookup"><span data-stu-id="c33f6-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-366">Resolução ao longo do eixo x (direção horizontal) do monitor.</span><span class="sxs-lookup"><span data-stu-id="c33f6-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-367">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="c33f6-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-368">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-370">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels por polegada lógica")</span><span class="sxs-lookup"><span data-stu-id="c33f6-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-371">Resolução ao longo do eixo y (direção vertical) do monitor.</span><span class="sxs-lookup"><span data-stu-id="c33f6-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c33f6-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-375">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c33f6-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-376">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c33f6-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c33f6-377">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c33f6-378">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c33f6-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-379">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c33f6-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-380">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c33f6-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-382">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c33f6-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c33f6-383">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c33f6-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c33f6-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c33f6-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="c33f6-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-386">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c33f6-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c33f6-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c33f6-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c33f6-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-389">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c33f6-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c33f6-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c33f6-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-391">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="c33f6-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c33f6-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="c33f6-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-393">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c33f6-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c33f6-394">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c33f6-395">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c33f6-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c33f6-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="c33f6-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-397">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="c33f6-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c33f6-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="c33f6-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c33f6-399">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="c33f6-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c33f6-400">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c33f6-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-401">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c33f6-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-403">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c33f6-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c33f6-404">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="c33f6-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c33f6-405">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-406">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="c33f6-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-407">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-409">Altura lógica da exibição em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="c33f6-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="c33f6-410">Essa propriedade é herdada do [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-411">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="c33f6-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-412">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33f6-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-414">Largura lógica da exibição em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="c33f6-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="c33f6-415">Essa propriedade é herdada do [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-416">**Status**</span><span class="sxs-lookup"><span data-stu-id="c33f6-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-417">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-419">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c33f6-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-420">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c33f6-420">Current status of the object.</span></span> <span data-ttu-id="c33f6-421">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c33f6-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c33f6-422">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c33f6-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c33f6-423">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c33f6-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c33f6-424">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c33f6-425">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c33f6-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c33f6-426">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c33f6-427">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c33f6-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c33f6-428">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c33f6-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c33f6-429">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c33f6-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c33f6-430">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c33f6-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c33f6-431">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c33f6-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c33f6-432">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c33f6-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c33f6-433">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c33f6-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c33f6-434">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c33f6-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c33f6-435">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c33f6-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c33f6-436">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c33f6-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c33f6-437">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c33f6-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c33f6-438">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c33f6-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c33f6-439">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c33f6-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c33f6-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c33f6-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-441">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c33f6-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-443">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="c33f6-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-444">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c33f6-444">State of the logical device.</span></span> <span data-ttu-id="c33f6-445">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c33f6-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c33f6-446">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c33f6-447">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c33f6-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c33f6-448">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c33f6-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c33f6-449">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c33f6-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c33f6-450">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c33f6-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c33f6-451">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="c33f6-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c33f6-452">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c33f6-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-453">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-455">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c33f6-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-456">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c33f6-457">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33f6-458">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c33f6-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c33f6-459">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c33f6-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c33f6-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c33f6-461">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c33f6-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c33f6-462">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c33f6-462">Name of the scoping system.</span></span>

<span data-ttu-id="c33f6-463">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c33f6-464">Comentários</span><span class="sxs-lookup"><span data-stu-id="c33f6-464">Remarks</span></span>

<span data-ttu-id="c33f6-465">A classe **Win32 \_ DesktopMonitor** é derivada de [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md), que deriva da [**\_ exibição de CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="c33f6-466">**CIM \_ A exibição** é derivada [**de \_ userdevice do CIM**](cim-userdevice.md), que deriva [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c33f6-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c33f6-467">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c33f6-467">Examples</span></span>

<span data-ttu-id="c33f6-468">O exemplo de [desenho de configuração de computador do PS usando](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) o PowerShell do Visio na galeria do TechNet usa o **Win32 \_ DesktopMonitor** para interagir com o modelo de automação do Visio para criar um desenho do Visio.</span><span class="sxs-lookup"><span data-stu-id="c33f6-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33f6-469">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c33f6-469">Requirements</span></span>



| <span data-ttu-id="c33f6-470">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33f6-470">Requirement</span></span> | <span data-ttu-id="c33f6-471">Valor</span><span class="sxs-lookup"><span data-stu-id="c33f6-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33f6-472">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c33f6-472">Minimum supported client</span></span><br/> | <span data-ttu-id="c33f6-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c33f6-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c33f6-474">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c33f6-474">Minimum supported server</span></span><br/> | <span data-ttu-id="c33f6-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c33f6-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c33f6-476">Namespace</span><span class="sxs-lookup"><span data-stu-id="c33f6-476">Namespace</span></span><br/>                | <span data-ttu-id="c33f6-477">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c33f6-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c33f6-478">MOF</span><span class="sxs-lookup"><span data-stu-id="c33f6-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c33f6-479"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c33f6-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c33f6-480">DLL</span><span class="sxs-lookup"><span data-stu-id="c33f6-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33f6-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c33f6-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33f6-482">Confira também</span><span class="sxs-lookup"><span data-stu-id="c33f6-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33f6-483">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="c33f6-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="c33f6-484">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c33f6-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c33f6-485">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="c33f6-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

