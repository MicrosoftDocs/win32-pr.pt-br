---
description: O Win32 \_ ParallelPort &\# 32; A classe WMI representa as propriedades de uma porta paralela em um sistema de computador que executa o Windows.
ms.assetid: 986bd27f-71b0-4a40-a421-a8bfc0f081be
ms.tgt_platform: multiple
title: Classe Win32_ParallelPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ParallelPort
- Win32_ParallelPort.Reset
- Win32_ParallelPort.SetPowerState
- Win32_ParallelPort.Availability
- Win32_ParallelPort.Capabilities
- Win32_ParallelPort.CapabilityDescriptions
- Win32_ParallelPort.Caption
- Win32_ParallelPort.ConfigManagerErrorCode
- Win32_ParallelPort.ConfigManagerUserConfig
- Win32_ParallelPort.CreationClassName
- Win32_ParallelPort.Description
- Win32_ParallelPort.DeviceID
- Win32_ParallelPort.DMASupport
- Win32_ParallelPort.ErrorCleared
- Win32_ParallelPort.ErrorDescription
- Win32_ParallelPort.InstallDate
- Win32_ParallelPort.LastErrorCode
- Win32_ParallelPort.MaxNumberControlled
- Win32_ParallelPort.Name
- Win32_ParallelPort.OSAutoDiscovered
- Win32_ParallelPort.PNPDeviceID
- Win32_ParallelPort.PowerManagementCapabilities
- Win32_ParallelPort.PowerManagementSupported
- Win32_ParallelPort.ProtocolSupported
- Win32_ParallelPort.Status
- Win32_ParallelPort.StatusInfo
- Win32_ParallelPort.SystemCreationClassName
- Win32_ParallelPort.SystemName
- Win32_ParallelPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da2ed3b34f3655067fd5ae41c31424e7599789c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089524"
---
# <a name="win32_parallelport-class"></a><span data-ttu-id="c901c-103">\_Classe Win32 ParallelPort</span><span class="sxs-lookup"><span data-stu-id="c901c-103">Win32\_ParallelPort class</span></span>

<span data-ttu-id="c901c-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ParallelPort do Win32** representa as propriedades de uma porta paralela em um sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="c901c-104">The **Win32\_ParallelPort** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a parallel port on a computer system running Windows.</span></span>

<span data-ttu-id="c901c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c901c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c901c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c901c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c901c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c901c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class  Win32_ParallelPort : CIM_ParallelController
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
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

## <a name="members"></a><span data-ttu-id="c901c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c901c-108">Members</span></span>

<span data-ttu-id="c901c-109">A classe **Win32 \_ ParallelPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c901c-109">The **Win32\_ParallelPort** class has these types of members:</span></span>

-   [<span data-ttu-id="c901c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c901c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c901c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c901c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c901c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c901c-112">Methods</span></span>

<span data-ttu-id="c901c-113">A classe **Win32 \_ ParallelPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c901c-113">The **Win32\_ParallelPort** class has these methods.</span></span>



| <span data-ttu-id="c901c-114">Método</span><span class="sxs-lookup"><span data-stu-id="c901c-114">Method</span></span>            | <span data-ttu-id="c901c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c901c-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c901c-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c901c-116">**Reset**</span></span>         | <span data-ttu-id="c901c-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c901c-117">Not implemented.</span></span> <span data-ttu-id="c901c-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="c901c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c901c-119">**SetPowerState**</span></span> | <span data-ttu-id="c901c-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c901c-120">Not implemented.</span></span> <span data-ttu-id="c901c-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c901c-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c901c-122">Properties</span></span>

<span data-ttu-id="c901c-123">A classe **Win32 \_ ParallelPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c901c-123">The **Win32\_ParallelPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c901c-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="c901c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c901c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c901c-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-128">Availability and status of the device.</span></span>

<span data-ttu-id="c901c-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c901c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c901c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c901c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c901c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c901c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="c901c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c901c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="c901c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c901c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="c901c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c901c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="c901c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c901c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="c901c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c901c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="c901c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c901c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="c901c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c901c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c901c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c901c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c901c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c901c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="c901c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c901c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="c901c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c901c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c901c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="c901c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="c901c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c901c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c901c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c901c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="c901c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c901c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="c901c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c901c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c901c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c901c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c901c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c901c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="c901c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="c901c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c901c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c901c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="c901c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c901c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="c901c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="c901c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-160">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="c901c-160">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-161">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c901c-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c901c-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-163">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|As portas paralelas DMTF \| 3,8 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="c901c-163">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-164">Matriz dos recursos do controlador paralelo.</span><span class="sxs-lookup"><span data-stu-id="c901c-164">Array of the capabilities of the parallel controller.</span></span>

<span data-ttu-id="c901c-165">Essa propriedade é herdada do [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-165">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901c-166">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c901c-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c901c-167">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c901c-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="c901c-168">**XT/at compatível** (2)</span><span class="sxs-lookup"><span data-stu-id="c901c-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="c901c-169">**Compatível com PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="c901c-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="c901c-170">**Ecp** (4)</span><span class="sxs-lookup"><span data-stu-id="c901c-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="c901c-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="c901c-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="c901c-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="c901c-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="c901c-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="c901c-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="c901c-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="c901c-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c901c-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-176">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c901c-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-178">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM ParallelController**](cim-parallelcontroller.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="c901c-178">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-179">Matriz de explicações mais detalhadas para qualquer um dos recursos do controlador paralelo indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c901c-179">Array of more detailed explanations for any of the parallel controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="c901c-180">Cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="c901c-180">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="c901c-181">Essa propriedade é herdada do [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-181">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-182">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c901c-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-185">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c901c-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-186">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="c901c-186">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="c901c-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c901c-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-189">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c901c-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-191">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c901c-191">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-192">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c901c-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c901c-193">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c901c-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c901c-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c901c-195"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="c901c-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-196">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c901c-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c901c-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c901c-198">(1)</span><span class="sxs-lookup"><span data-stu-id="c901c-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-199">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c901c-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c901c-201">(2)</span><span class="sxs-lookup"><span data-stu-id="c901c-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c901c-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c901c-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c901c-203">(3)</span><span class="sxs-lookup"><span data-stu-id="c901c-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-204">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="c901c-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c901c-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c901c-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c901c-206">(4)</span><span class="sxs-lookup"><span data-stu-id="c901c-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-207">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-207">Device is not working properly.</span></span> <span data-ttu-id="c901c-208">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c901c-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c901c-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="c901c-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c901c-210">(5)</span><span class="sxs-lookup"><span data-stu-id="c901c-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-211">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="c901c-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c901c-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c901c-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c901c-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="c901c-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-214">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c901c-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c901c-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c901c-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c901c-216">(7)</span><span class="sxs-lookup"><span data-stu-id="c901c-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c901c-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="c901c-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c901c-218">(8)</span><span class="sxs-lookup"><span data-stu-id="c901c-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-219">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="c901c-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c901c-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="c901c-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c901c-221">(9)</span><span class="sxs-lookup"><span data-stu-id="c901c-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-222">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-222">Device is not working properly.</span></span> <span data-ttu-id="c901c-223">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c901c-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="c901c-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c901c-225">(10)</span><span class="sxs-lookup"><span data-stu-id="c901c-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-226">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c901c-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="c901c-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c901c-228">(11)</span><span class="sxs-lookup"><span data-stu-id="c901c-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-229">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c901c-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="c901c-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c901c-231">12</span><span class="sxs-lookup"><span data-stu-id="c901c-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-232">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="c901c-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c901c-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c901c-234">(13)</span><span class="sxs-lookup"><span data-stu-id="c901c-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-235">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c901c-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="c901c-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c901c-237">(14)</span><span class="sxs-lookup"><span data-stu-id="c901c-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-238">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c901c-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c901c-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="c901c-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c901c-240">(15)</span><span class="sxs-lookup"><span data-stu-id="c901c-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-241">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="c901c-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c901c-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="c901c-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c901c-243">(16)</span><span class="sxs-lookup"><span data-stu-id="c901c-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-244">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="c901c-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c901c-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="c901c-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c901c-246">(17)</span><span class="sxs-lookup"><span data-stu-id="c901c-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-247">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c901c-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c901c-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c901c-249">(18)</span><span class="sxs-lookup"><span data-stu-id="c901c-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-250">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="c901c-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c901c-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="c901c-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c901c-252">(19)</span><span class="sxs-lookup"><span data-stu-id="c901c-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c901c-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c901c-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c901c-254">(20)</span><span class="sxs-lookup"><span data-stu-id="c901c-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-255">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c901c-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c901c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c901c-257">(21)</span><span class="sxs-lookup"><span data-stu-id="c901c-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-258">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c901c-258">System failure.</span></span> <span data-ttu-id="c901c-259">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c901c-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c901c-260">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c901c-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c901c-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c901c-262">(22)</span><span class="sxs-lookup"><span data-stu-id="c901c-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-263">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c901c-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c901c-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="c901c-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c901c-265">(23)</span><span class="sxs-lookup"><span data-stu-id="c901c-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-266">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c901c-266">System failure.</span></span> <span data-ttu-id="c901c-267">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c901c-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c901c-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="c901c-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c901c-269">(24)</span><span class="sxs-lookup"><span data-stu-id="c901c-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-270">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="c901c-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c901c-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c901c-272">(25)</span><span class="sxs-lookup"><span data-stu-id="c901c-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-273">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c901c-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c901c-275">(26)</span><span class="sxs-lookup"><span data-stu-id="c901c-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-276">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c901c-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c901c-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="c901c-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c901c-278">(27)</span><span class="sxs-lookup"><span data-stu-id="c901c-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-279">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="c901c-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c901c-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="c901c-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c901c-281">(28)</span><span class="sxs-lookup"><span data-stu-id="c901c-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-282">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="c901c-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c901c-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="c901c-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c901c-284">(29)</span><span class="sxs-lookup"><span data-stu-id="c901c-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-285">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c901c-285">Device is disabled.</span></span> <span data-ttu-id="c901c-286">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="c901c-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c901c-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c901c-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c901c-288">(30)</span><span class="sxs-lookup"><span data-stu-id="c901c-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-289">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="c901c-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c901c-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c901c-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c901c-291">(31)</span><span class="sxs-lookup"><span data-stu-id="c901c-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-292">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-292">Device is not working properly.</span></span> <span data-ttu-id="c901c-293">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="c901c-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c901c-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-295">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c901c-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-297">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c901c-297">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-298">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c901c-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c901c-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c901c-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-303">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c901c-303">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c901c-304">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c901c-304">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c901c-305">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c901c-305">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="c901c-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-307">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c901c-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-310">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c901c-310">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-311">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c901c-311">Description of the object.</span></span>

<span data-ttu-id="c901c-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c901c-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-316">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c901c-316">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-317">Identificador da porta paralela.</span><span class="sxs-lookup"><span data-stu-id="c901c-317">Identifier of the parallel port.</span></span>

<span data-ttu-id="c901c-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-319">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="c901c-319">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-320">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c901c-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-322">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Portas paralelas DMTF \| 3,7 ")</span><span class="sxs-lookup"><span data-stu-id="c901c-322">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-323">Se **for true**, a porta paralela oferece suporte a DMA.</span><span class="sxs-lookup"><span data-stu-id="c901c-323">If **TRUE**, the parallel port supports DMA.</span></span>

<span data-ttu-id="c901c-324">Essa propriedade é herdada do [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-324">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c901c-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-326">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c901c-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c901c-328">Se **for true**, o erro relatado em **LastErrorCode** será limpo.</span><span class="sxs-lookup"><span data-stu-id="c901c-328">If **TRUE**, the error reported in **LastErrorCode** is cleared.</span></span>

<span data-ttu-id="c901c-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c901c-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c901c-333">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="c901c-333">More information about the error recorded in **LastErrorCode**, and information about corrective actions that might be taken.</span></span>

<span data-ttu-id="c901c-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c901c-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-336">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c901c-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-338">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c901c-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-339">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c901c-339">Date and time the object was installed.</span></span> <span data-ttu-id="c901c-340">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c901c-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c901c-341">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c901c-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-343">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c901c-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c901c-345">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c901c-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c901c-346">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-347">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="c901c-347">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-348">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c901c-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-350">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="c901c-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-351">Número máximo de entidades diretamente endereçáveis com suporte por este controlador.</span><span class="sxs-lookup"><span data-stu-id="c901c-351">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="c901c-352">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c901c-352">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="c901c-353">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-353">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-354">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c901c-354">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-357">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c901c-357">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-358">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c901c-358">Label by which the object is known.</span></span> <span data-ttu-id="c901c-359">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c901c-359">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c901c-360">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-360">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-361">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="c901c-361">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-362">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c901c-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-364">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c901c-364">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-365">Se **for true**, a porta paralela foi detectada automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c901c-365">If **TRUE**, the parallel port was automatically detected by the operating system.</span></span> <span data-ttu-id="c901c-366">Se **for false**, a porta foi detectada por outros meios (por exemplo, sendo adicionada manualmente por meio do painel de controle).</span><span class="sxs-lookup"><span data-stu-id="c901c-366">If **FALSE**, the port was detected by other means (such as being manually added through the Control Panel).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-367">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c901c-367">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-368">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-370">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c901c-370">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-371">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c901c-371">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c901c-372">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c901c-373">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c901c-373">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c901c-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c901c-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-375">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c901c-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c901c-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c901c-377">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c901c-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c901c-378">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="c901c-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901c-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c901c-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c901c-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="c901c-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c901c-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c901c-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c901c-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c901c-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-383">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c901c-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c901c-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c901c-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-385">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="c901c-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c901c-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="c901c-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-387">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c901c-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c901c-388">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="c901c-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c901c-389">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-389">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c901c-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="c901c-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-391">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="c901c-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c901c-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="c901c-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c901c-393">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="c901c-393">Timed Power-On Supported</span></span>

<span data-ttu-id="c901c-394">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="c901c-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c901c-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-396">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c901c-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c901c-398">Se **for true**, o dispositivo poderá ser gerenciado por energia, o que significa que ele pode ser colocado no modo de suspensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c901c-398">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="c901c-399">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="c901c-399">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c901c-400">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-401">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="c901c-401">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-402">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c901c-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-404">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="c901c-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-405">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="c901c-405">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="c901c-406">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-406">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="c901c-407">Os valores são mostrados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="c901c-407">Values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c901c-408">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c901c-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901c-409">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c901c-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="c901c-410">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c901c-410">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="c901c-411">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="c901c-411">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="c901c-412">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="c901c-412">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="c901c-413">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="c901c-413">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="c901c-414">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="c901c-414">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="c901c-415">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="c901c-415">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="c901c-416">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="c901c-416">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="c901c-417">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="c901c-417">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="c901c-418">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="c901c-418">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="c901c-419">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="c901c-419">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="c901c-420">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="c901c-420">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="c901c-421">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="c901c-421">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="c901c-422">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="c901c-422">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="c901c-423">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="c901c-423">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="c901c-424">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="c901c-424">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="c901c-425">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="c901c-425">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="c901c-426">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="c901c-426">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="c901c-427">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="c901c-427">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c901c-428">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="c901c-428">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="c901c-429">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="c901c-429">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="c901c-430">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="c901c-430">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="c901c-431">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="c901c-431">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="c901c-432">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="c901c-432">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="c901c-433">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="c901c-433">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="c901c-434">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="c901c-434">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="c901c-435">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="c901c-435">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="c901c-436">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="c901c-436">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="c901c-437">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="c901c-437">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="c901c-438">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="c901c-438">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="c901c-439">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="c901c-439">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="c901c-440">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="c901c-440">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="c901c-441">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="c901c-441">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="c901c-442">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="c901c-442">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="c901c-443">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="c901c-443">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="c901c-444">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="c901c-444">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="c901c-445">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="c901c-445">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="c901c-446">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="c901c-446">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="c901c-447">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="c901c-447">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="c901c-448">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="c901c-448">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="c901c-449">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="c901c-449">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="c901c-450">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="c901c-450">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="c901c-451">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="c901c-451">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="c901c-452">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="c901c-452">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="c901c-453">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="c901c-453">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="c901c-454">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="c901c-454">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-455">**Status**</span><span class="sxs-lookup"><span data-stu-id="c901c-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-456">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-458">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="c901c-458">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-459">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c901c-459">Current status of the object.</span></span> <span data-ttu-id="c901c-460">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c901c-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c901c-461">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c901c-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c901c-462">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c901c-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c901c-463">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c901c-463">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c901c-464">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c901c-464">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c901c-465">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c901c-466">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c901c-466">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c901c-467">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c901c-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c901c-468">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c901c-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c901c-469">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c901c-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901c-470">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c901c-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c901c-471">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c901c-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c901c-472">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c901c-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c901c-473">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c901c-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c901c-474">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c901c-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c901c-475">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c901c-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c901c-476">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c901c-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c901c-477">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c901c-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c901c-478">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c901c-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c901c-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-480">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c901c-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-482">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="c901c-482">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c901c-483">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c901c-483">State of the logical device.</span></span> <span data-ttu-id="c901c-484">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c901c-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c901c-485">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c901c-486">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c901c-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c901c-487">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c901c-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c901c-488">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c901c-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c901c-489">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c901c-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c901c-490">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="c901c-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c901c-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c901c-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-492">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-494">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c901c-494">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c901c-495">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="c901c-495">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c901c-496">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-496">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-497">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c901c-497">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-498">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c901c-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c901c-500">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c901c-500">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c901c-501">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c901c-501">Name of the scoping system.</span></span>

<span data-ttu-id="c901c-502">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c901c-503">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c901c-503">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c901c-504">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c901c-504">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c901c-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c901c-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c901c-506">Data e hora da última redefinição do controlador.</span><span class="sxs-lookup"><span data-stu-id="c901c-506">Date and time the controller was last reset.</span></span> <span data-ttu-id="c901c-507">Isso pode significar que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="c901c-507">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="c901c-508">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-508">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c901c-509">Comentários</span><span class="sxs-lookup"><span data-stu-id="c901c-509">Remarks</span></span>

<span data-ttu-id="c901c-510">A classe **Win32 \_ ParallelPort** é derivada de [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="c901c-510">The **Win32\_ParallelPort** class is derived from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c901c-511">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c901c-511">Requirements</span></span>



| <span data-ttu-id="c901c-512">Requisito</span><span class="sxs-lookup"><span data-stu-id="c901c-512">Requirement</span></span> | <span data-ttu-id="c901c-513">Valor</span><span class="sxs-lookup"><span data-stu-id="c901c-513">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c901c-514">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c901c-514">Minimum supported client</span></span><br/> | <span data-ttu-id="c901c-515">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c901c-515">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c901c-516">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c901c-516">Minimum supported server</span></span><br/> | <span data-ttu-id="c901c-517">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c901c-517">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c901c-518">Namespace</span><span class="sxs-lookup"><span data-stu-id="c901c-518">Namespace</span></span><br/>                | <span data-ttu-id="c901c-519">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c901c-519">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c901c-520">MOF</span><span class="sxs-lookup"><span data-stu-id="c901c-520">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c901c-521"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c901c-521"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c901c-522">DLL</span><span class="sxs-lookup"><span data-stu-id="c901c-522">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c901c-523"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c901c-523"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c901c-524">Confira também</span><span class="sxs-lookup"><span data-stu-id="c901c-524">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c901c-525">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="c901c-525">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dt>

[<span data-ttu-id="c901c-526">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c901c-526">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
