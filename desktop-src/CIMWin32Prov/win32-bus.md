---
description: A \_ classe WMI de barramento Win32 representa um barramento físico como visto por um computador que executa um sistema operacional Windows. Qualquer instância de um barramento do Windows é um descendente (ou membro) dessa classe.
ms.assetid: 76ba15f4-8c7b-4713-b5a2-e444fbab064a
ms.tgt_platform: multiple
title: Classe Win32_Bus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Bus
- Win32_Bus.Reset
- Win32_Bus.SetPowerState
- Win32_Bus.Availability
- Win32_Bus.BusNum
- Win32_Bus.BusType
- Win32_Bus.Caption
- Win32_Bus.ConfigManagerErrorCode
- Win32_Bus.ConfigManagerUserConfig
- Win32_Bus.CreationClassName
- Win32_Bus.Description
- Win32_Bus.DeviceID
- Win32_Bus.ErrorCleared
- Win32_Bus.ErrorDescription
- Win32_Bus.InstallDate
- Win32_Bus.LastErrorCode
- Win32_Bus.Name
- Win32_Bus.PNPDeviceID
- Win32_Bus.PowerManagementCapabilities
- Win32_Bus.PowerManagementSupported
- Win32_Bus.Status
- Win32_Bus.StatusInfo
- Win32_Bus.SystemCreationClassName
- Win32_Bus.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac31a2187ee7e4974e1ddedbf084efd482748753
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826244"
---
# <a name="win32_bus-class"></a><span data-ttu-id="4e1e9-104">\_Classe de barramento Win32</span><span class="sxs-lookup"><span data-stu-id="4e1e9-104">Win32\_Bus class</span></span>

<span data-ttu-id="4e1e9-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ barramento Win32** representa um barramento físico como visto por um computador que executa um sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-105">The **Win32\_Bus** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical bus as seen by a computer running a Windows operating system.</span></span> <span data-ttu-id="4e1e9-106">Qualquer instância de um barramento do Windows é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-106">Any instance of a Windows bus is a descendant (or member) of this class.</span></span>

<span data-ttu-id="4e1e9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1e9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e1e9-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Bus : CIM_LogicalDevice
{
  uint16   Availability;
  uint32   BusNum;
  uint32   BusType;
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="4e1e9-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4e1e9-109">Members</span></span>

<span data-ttu-id="4e1e9-110">A classe de **\_ barramento Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4e1e9-110">The **Win32\_Bus** class has these types of members:</span></span>

-   [<span data-ttu-id="4e1e9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e1e9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e1e9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e1e9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e1e9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e1e9-113">Methods</span></span>

<span data-ttu-id="4e1e9-114">A classe de **\_ barramento Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-114">The **Win32\_Bus** class has these methods.</span></span>



| <span data-ttu-id="4e1e9-115">Método</span><span class="sxs-lookup"><span data-stu-id="4e1e9-115">Method</span></span>            | <span data-ttu-id="4e1e9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e1e9-116">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1e9-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-117">**Reset**</span></span>         | <span data-ttu-id="4e1e9-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-118">Not implemented.</span></span> <span data-ttu-id="4e1e9-119">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ LogicalDevice CIM**](cim-logicaldevice.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="4e1e9-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-120">**SetPowerState**</span></span> | <span data-ttu-id="4e1e9-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-121">Not implemented.</span></span> <span data-ttu-id="4e1e9-122">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ LogicalDevice CIM**](cim-logicaldevice.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e1e9-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e1e9-123">Properties</span></span>

<span data-ttu-id="4e1e9-124">A classe de **\_ barramento Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-124">The **Win32\_Bus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e1e9-125">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-129">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-129">Availability and status of the device.</span></span>

<span data-ttu-id="4e1e9-130">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e1e9-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e1e9-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4e1e9-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-134">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="4e1e9-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4e1e9-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4e1e9-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4e1e9-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4e1e9-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="4e1e9-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4e1e9-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4e1e9-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e1e9-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4e1e9-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4e1e9-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4e1e9-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4e1e9-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4e1e9-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4e1e9-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4e1e9-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4e1e9-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4e1e9-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4e1e9-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4e1e9-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e1e9-161">**BusNum**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-161">**BusNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-164">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-165">Número lógico atribuído ao barramento físico.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-165">Logical number assigned to the physical bus.</span></span>

<span data-ttu-id="4e1e9-166">Example: 1</span><span class="sxs-lookup"><span data-stu-id="4e1e9-166">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-167">**BusType**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-167">**BusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-170">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| cHwRes \| interface \_ Type")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|cHwRes\|INTERFACE\_TYPE")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-171">Tipo do barramento físico.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-171">Type of the physical bus.</span></span> <span data-ttu-id="4e1e9-172">Esse valor será um dos valores na enumeração de **\_ tipo de interface** definida em Bus. h.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-172">This value will be one of the values in the **INTERFACE\_TYPE** enumeration defined in Bus.h.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="4e1e9-173">**Indefinido** (-1)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-173">**Undefined** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="4e1e9-174">**Interno** (0)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-174">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="4e1e9-175">**ISA** (1)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-175">**ISA** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="4e1e9-176">**EISA** (2)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-176">**EISA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MicroChannel"></span><span id="microchannel"></span><span id="MICROCHANNEL"></span>

<span data-ttu-id="4e1e9-177">**Microchannel** (3)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-177">**MicroChannel** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboChannel"></span><span id="turbochannel"></span><span id="TURBOCHANNEL"></span>

<span data-ttu-id="4e1e9-178">**TurboChannel** (4)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-178">**TurboChannel** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Bus"></span><span id="pci_bus"></span><span id="PCI_BUS"></span>

<span data-ttu-id="4e1e9-179">**Barramento PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-179">**PCI Bus** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="4e1e9-180">**Barramento de VM** (6)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-180">**VME Bus** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="4e1e9-181">**NuBus** (7)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-181">**NuBus** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Bus"></span><span id="pcmcia_bus"></span><span id="PCMCIA_BUS"></span>

<span data-ttu-id="4e1e9-182">**Barramento PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-182">**PCMCIA Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="C_Bus"></span><span id="c_bus"></span><span id="C_BUS"></span>

<span data-ttu-id="4e1e9-183">**Barramento C** (9)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-183">**C Bus** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MPI_Bus"></span><span id="mpi_bus"></span><span id="MPI_BUS"></span>

<span data-ttu-id="4e1e9-184">**Barramento MPI** (10)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-184">**MPI Bus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MPSA_Bus"></span><span id="mpsa_bus"></span><span id="MPSA_BUS"></span>

<span data-ttu-id="4e1e9-185">**Barramento MPSA** (11)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-185">**MPSA Bus** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Processor"></span><span id="internal_processor"></span><span id="INTERNAL_PROCESSOR"></span>

<span data-ttu-id="4e1e9-186">**Processador interno** (12)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-186">**Internal Processor** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Power_Bus"></span><span id="internal_power_bus"></span><span id="INTERNAL_POWER_BUS"></span>

<span data-ttu-id="4e1e9-187">**Barramento de energia interno** (13)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-187">**Internal Power Bus** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_ISA_Bus"></span><span id="pnp_isa_bus"></span><span id="PNP_ISA_BUS"></span>

<span data-ttu-id="4e1e9-188">**Barramento PnP ISA** (14)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-188">**PNP ISA Bus** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_Bus"></span><span id="pnp_bus"></span><span id="PNP_BUS"></span>

<span data-ttu-id="4e1e9-189">**Barramento PnP** (15)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-189">**PNP Bus** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum_Interface_Type"></span><span id="maximum_interface_type"></span><span id="MAXIMUM_INTERFACE_TYPE"></span>

<span data-ttu-id="4e1e9-190">**Tipo de interface máximo** (16)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-190">**Maximum Interface Type** (16)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e1e9-191">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-194">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-195">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-195">Short description of the object a one-line string.</span></span>

<span data-ttu-id="4e1e9-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-197">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-198">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-200">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-201">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-201">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="4e1e9-202">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4e1e9-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4e1e9-204"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-205">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4e1e9-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4e1e9-207">(1)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-208">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4e1e9-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4e1e9-210">(2)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4e1e9-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4e1e9-212">(3)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-213">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4e1e9-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4e1e9-215">(4)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-216">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-216">Device is not working properly.</span></span> <span data-ttu-id="4e1e9-217">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4e1e9-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4e1e9-219">(5)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-220">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4e1e9-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4e1e9-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-223">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4e1e9-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4e1e9-225">(7)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4e1e9-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4e1e9-227">(8)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-228">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4e1e9-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4e1e9-230">(9)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-231">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-231">Device is not working properly.</span></span> <span data-ttu-id="4e1e9-232">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-232">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4e1e9-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4e1e9-234">(10)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-234">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-235">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-235">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4e1e9-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4e1e9-237">(11)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-237">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-238">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-238">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4e1e9-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4e1e9-240">12</span><span class="sxs-lookup"><span data-stu-id="4e1e9-240">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-241">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-241">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4e1e9-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4e1e9-243">(13)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-243">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-244">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-244">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4e1e9-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4e1e9-246">(14)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-246">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-247">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-247">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4e1e9-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4e1e9-249">(15)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-249">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-250">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-250">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4e1e9-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4e1e9-252">(16)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-252">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-253">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-253">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4e1e9-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4e1e9-255">(17)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-255">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-256">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-256">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4e1e9-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4e1e9-258">(18)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-258">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-259">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-259">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4e1e9-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4e1e9-261">(19)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-261">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4e1e9-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4e1e9-263">(20)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-263">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-264">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-264">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4e1e9-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4e1e9-266">(21)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-266">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-267">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-267">System failure.</span></span> <span data-ttu-id="4e1e9-268">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-268">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4e1e9-269">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-269">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4e1e9-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4e1e9-271">(22)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-271">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-272">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-272">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4e1e9-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4e1e9-274">(23)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-274">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-275">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-275">System failure.</span></span> <span data-ttu-id="4e1e9-276">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-276">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4e1e9-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4e1e9-278">(24)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-278">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-279">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-279">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4e1e9-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4e1e9-281">(25)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-281">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-282">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-282">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4e1e9-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4e1e9-284">(26)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-284">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-285">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-285">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4e1e9-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4e1e9-287">(27)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-287">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-288">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-288">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4e1e9-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4e1e9-290">(28)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-290">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-291">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-291">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4e1e9-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4e1e9-293">(29)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-293">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-294">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-294">Device is disabled.</span></span> <span data-ttu-id="4e1e9-295">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-295">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4e1e9-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4e1e9-297">(30)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-297">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-298">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-298">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4e1e9-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4e1e9-300">(31)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-300">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-301">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-301">Device is not working properly.</span></span> <span data-ttu-id="4e1e9-302">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-302">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e1e9-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-304">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-306">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-307">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4e1e9-308">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-309">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-309">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-312">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-313">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-313">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4e1e9-314">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-314">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="4e1e9-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-316">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-316">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-319">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-319">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-320">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-320">Description of the object.</span></span>

<span data-ttu-id="4e1e9-321">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-322">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-322">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-325">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-325">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-326">Nome exclusivo que identifica o barramento.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-326">Unique name that identifies the bus.</span></span>

<span data-ttu-id="4e1e9-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-328">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-328">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-329">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-331">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-331">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="4e1e9-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-333">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-333">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-336">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-336">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="4e1e9-337">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-339">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-341">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-342">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-342">Date and time the object was installed.</span></span> <span data-ttu-id="4e1e9-343">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4e1e9-344">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-346">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-348">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4e1e9-349">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-350">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-353">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-354">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-354">Label by which the object is known.</span></span> <span data-ttu-id="4e1e9-355">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4e1e9-356">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-357">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-357">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-360">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-360">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-361">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-361">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4e1e9-362">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4e1e9-363">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4e1e9-363">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-364">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-364">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-365">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-365">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-367">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-367">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4e1e9-368">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-368">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e1e9-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4e1e9-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e1e9-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4e1e9-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-373">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-373">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4e1e9-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-375">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-375">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4e1e9-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-377">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="4e1e9-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4e1e9-378">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-378">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4e1e9-379">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-379">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4e1e9-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-381">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-381">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4e1e9-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4e1e9-383">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="4e1e9-383">Timed Power-On Supported</span></span>

<span data-ttu-id="4e1e9-384">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e1e9-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-386">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-388">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-388">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="4e1e9-389">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-389">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="4e1e9-390">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-391">**Status**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-391">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-392">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-394">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-394">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-395">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-395">Current status of the object.</span></span> <span data-ttu-id="4e1e9-396">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-396">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4e1e9-397">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-397">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4e1e9-398">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="4e1e9-398">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4e1e9-399">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-399">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4e1e9-400">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-400">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4e1e9-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4e1e9-402">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4e1e9-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4e1e9-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4e1e9-404">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e1e9-405">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e1e9-406">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4e1e9-407">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4e1e9-408">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4e1e9-409">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4e1e9-410">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4e1e9-411">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4e1e9-412">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4e1e9-413">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4e1e9-414">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e1e9-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-416">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-418">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="4e1e9-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-419">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-419">State of the logical device.</span></span> <span data-ttu-id="4e1e9-420">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4e1e9-421">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e1e9-422">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e1e9-423">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4e1e9-424">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e1e9-425">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4e1e9-426">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e1e9-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-430">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-431">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-431">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="4e1e9-432">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e9-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1e9-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e1e9-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1e9-436">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e1e9-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e1e9-437">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="4e1e9-437">Name of the scoping system.</span></span>

<span data-ttu-id="4e1e9-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e1e9-439">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e1e9-439">Remarks</span></span>

<span data-ttu-id="4e1e9-440">A classe de **\_ barramento Win32** é derivada [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e1e9-440">The **Win32\_Bus** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1e9-441">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e1e9-441">Requirements</span></span>



| <span data-ttu-id="4e1e9-442">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e1e9-442">Requirement</span></span> | <span data-ttu-id="4e1e9-443">Valor</span><span class="sxs-lookup"><span data-stu-id="4e1e9-443">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1e9-444">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e1e9-444">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1e9-445">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e1e9-445">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e1e9-446">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e1e9-446">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1e9-447">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e1e9-447">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e1e9-448">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e1e9-448">Namespace</span></span><br/>                | <span data-ttu-id="4e1e9-449">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4e1e9-449">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e1e9-450">MOF</span><span class="sxs-lookup"><span data-stu-id="4e1e9-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e1e9-451"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e1e9-451"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e1e9-452">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1e9-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e1e9-453"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e1e9-453"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1e9-454">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e1e9-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1e9-455">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4e1e9-455">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="4e1e9-456">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="4e1e9-456">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

