---
description: A \_ classe WMI SCSIController do Win32 representa um controlador SCSI em um sistema de computador executando o Windows.
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Classe Win32_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811148"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="202b2-103">\_Classe Win32 SCSIController</span><span class="sxs-lookup"><span data-stu-id="202b2-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="202b2-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SCSIController do Win32** representa um controlador SCSI em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="202b2-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="202b2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="202b2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="202b2-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="202b2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="202b2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="202b2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="202b2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="202b2-108">Members</span></span>

<span data-ttu-id="202b2-109">A classe **Win32 \_ SCSIController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="202b2-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="202b2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="202b2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="202b2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="202b2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="202b2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="202b2-112">Methods</span></span>

<span data-ttu-id="202b2-113">A classe **Win32 \_ SCSIController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="202b2-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="202b2-114">Método</span><span class="sxs-lookup"><span data-stu-id="202b2-114">Method</span></span>            | <span data-ttu-id="202b2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="202b2-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202b2-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="202b2-116">**Reset**</span></span>         | <span data-ttu-id="202b2-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="202b2-117">Not implemented.</span></span> <span data-ttu-id="202b2-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="202b2-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="202b2-119">**SetPowerState**</span></span> | <span data-ttu-id="202b2-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="202b2-120">Not implemented.</span></span> <span data-ttu-id="202b2-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="202b2-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="202b2-122">Properties</span></span>

<span data-ttu-id="202b2-123">A classe **Win32 \_ SCSIController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="202b2-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="202b2-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="202b2-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="202b2-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="202b2-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-128">Availability and status of the device.</span></span>

<span data-ttu-id="202b2-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="202b2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="202b2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="202b2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="202b2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="202b2-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="202b2-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="202b2-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="202b2-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="202b2-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="202b2-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="202b2-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="202b2-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="202b2-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="202b2-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="202b2-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="202b2-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="202b2-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="202b2-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="202b2-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="202b2-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="202b2-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="202b2-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="202b2-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="202b2-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="202b2-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="202b2-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="202b2-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="202b2-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="202b2-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="202b2-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="202b2-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="202b2-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="202b2-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="202b2-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="202b2-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="202b2-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="202b2-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="202b2-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="202b2-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="202b2-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="202b2-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="202b2-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="202b2-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="202b2-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="202b2-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="202b2-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="202b2-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="202b2-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="202b2-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="202b2-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-160">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="202b2-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-163">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="202b2-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-164">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="202b2-164">Short description of the object.</span></span>

<span data-ttu-id="202b2-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="202b2-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="202b2-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-169">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="202b2-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-170">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="202b2-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="202b2-171">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="202b2-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="202b2-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="202b2-173"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="202b2-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-174">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="202b2-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="202b2-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="202b2-176">(1)</span><span class="sxs-lookup"><span data-stu-id="202b2-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-177">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="202b2-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="202b2-179">(2)</span><span class="sxs-lookup"><span data-stu-id="202b2-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="202b2-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="202b2-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="202b2-181">(3)</span><span class="sxs-lookup"><span data-stu-id="202b2-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-182">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="202b2-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="202b2-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="202b2-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="202b2-184">(4)</span><span class="sxs-lookup"><span data-stu-id="202b2-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-185">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-185">Device is not working properly.</span></span> <span data-ttu-id="202b2-186">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="202b2-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="202b2-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="202b2-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="202b2-188">(5)</span><span class="sxs-lookup"><span data-stu-id="202b2-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-189">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="202b2-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="202b2-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="202b2-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="202b2-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="202b2-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-192">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="202b2-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="202b2-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="202b2-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="202b2-194">(7)</span><span class="sxs-lookup"><span data-stu-id="202b2-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="202b2-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="202b2-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="202b2-196">(8)</span><span class="sxs-lookup"><span data-stu-id="202b2-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-197">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="202b2-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="202b2-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="202b2-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="202b2-199">(9)</span><span class="sxs-lookup"><span data-stu-id="202b2-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-200">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-200">Device is not working properly.</span></span> <span data-ttu-id="202b2-201">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="202b2-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="202b2-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="202b2-203">(10)</span><span class="sxs-lookup"><span data-stu-id="202b2-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-204">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="202b2-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="202b2-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="202b2-206">(11)</span><span class="sxs-lookup"><span data-stu-id="202b2-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-207">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="202b2-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="202b2-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="202b2-209">12</span><span class="sxs-lookup"><span data-stu-id="202b2-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-210">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="202b2-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="202b2-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="202b2-212">(13)</span><span class="sxs-lookup"><span data-stu-id="202b2-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-213">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="202b2-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="202b2-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="202b2-215">(14)</span><span class="sxs-lookup"><span data-stu-id="202b2-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-216">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="202b2-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="202b2-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="202b2-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="202b2-218">(15)</span><span class="sxs-lookup"><span data-stu-id="202b2-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-219">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="202b2-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="202b2-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="202b2-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="202b2-221">(16)</span><span class="sxs-lookup"><span data-stu-id="202b2-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-222">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="202b2-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="202b2-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="202b2-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="202b2-224">(17)</span><span class="sxs-lookup"><span data-stu-id="202b2-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-225">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="202b2-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="202b2-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="202b2-227">(18)</span><span class="sxs-lookup"><span data-stu-id="202b2-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-228">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="202b2-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="202b2-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="202b2-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="202b2-230">(19)</span><span class="sxs-lookup"><span data-stu-id="202b2-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="202b2-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="202b2-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="202b2-232">(20)</span><span class="sxs-lookup"><span data-stu-id="202b2-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-233">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="202b2-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="202b2-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="202b2-235">(21)</span><span class="sxs-lookup"><span data-stu-id="202b2-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-236">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="202b2-236">System failure.</span></span> <span data-ttu-id="202b2-237">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="202b2-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="202b2-238">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="202b2-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="202b2-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="202b2-240">(22)</span><span class="sxs-lookup"><span data-stu-id="202b2-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-241">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="202b2-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="202b2-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="202b2-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="202b2-243">(23)</span><span class="sxs-lookup"><span data-stu-id="202b2-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="202b2-244">System failure.</span></span> <span data-ttu-id="202b2-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="202b2-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="202b2-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="202b2-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="202b2-247">(24)</span><span class="sxs-lookup"><span data-stu-id="202b2-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-248">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="202b2-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="202b2-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="202b2-250">(25)</span><span class="sxs-lookup"><span data-stu-id="202b2-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-251">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="202b2-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="202b2-253">(26)</span><span class="sxs-lookup"><span data-stu-id="202b2-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-254">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="202b2-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="202b2-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="202b2-256">(27)</span><span class="sxs-lookup"><span data-stu-id="202b2-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-257">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="202b2-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="202b2-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="202b2-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="202b2-259">(28)</span><span class="sxs-lookup"><span data-stu-id="202b2-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-260">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="202b2-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="202b2-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="202b2-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="202b2-262">(29)</span><span class="sxs-lookup"><span data-stu-id="202b2-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-263">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="202b2-263">Device is disabled.</span></span> <span data-ttu-id="202b2-264">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="202b2-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="202b2-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="202b2-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="202b2-266">(30)</span><span class="sxs-lookup"><span data-stu-id="202b2-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-267">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="202b2-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="202b2-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="202b2-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="202b2-269">(31)</span><span class="sxs-lookup"><span data-stu-id="202b2-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-270">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-270">Device is not working properly.</span></span> <span data-ttu-id="202b2-271">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="202b2-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="202b2-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-273">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="202b2-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-275">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="202b2-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-276">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="202b2-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="202b2-277">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-278">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="202b2-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-279">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="202b2-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-281">Número de tempos limite que ocorreram após o valor de **TimeOfLastReset** .</span><span class="sxs-lookup"><span data-stu-id="202b2-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="202b2-282">Essa propriedade é herdada do [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="202b2-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-286">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="202b2-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="202b2-287">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="202b2-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="202b2-288">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="202b2-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="202b2-289">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-290">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="202b2-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-293">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="202b2-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-294">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="202b2-294">Description of the object.</span></span>

<span data-ttu-id="202b2-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="202b2-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-299">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| hardware \\ \\ DeviceMap \\ \\ SCSI")</span><span class="sxs-lookup"><span data-stu-id="202b2-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-300">Identificador exclusivo do controlador SCSI com outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="202b2-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="202b2-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-302">**DeviceMap**</span><span class="sxs-lookup"><span data-stu-id="202b2-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-305">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SCSI \| ScsiPort")</span><span class="sxs-lookup"><span data-stu-id="202b2-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-306">Ordem em que os dispositivos são listados com este controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="202b2-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="202b2-307">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="202b2-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-310">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| PortDriver")</span><span class="sxs-lookup"><span data-stu-id="202b2-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-311">Nome do arquivo do driver do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="202b2-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="202b2-312">Exemplo: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="202b2-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="202b2-313">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="202b2-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-314">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="202b2-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-316">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="202b2-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="202b2-317">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="202b2-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-321">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="202b2-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="202b2-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="202b2-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-326">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| HWRevision")</span><span class="sxs-lookup"><span data-stu-id="202b2-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-327">Número de versão de hardware do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="202b2-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="202b2-328">Exemplo: "1,25"</span><span class="sxs-lookup"><span data-stu-id="202b2-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="202b2-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="202b2-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-330">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="202b2-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-332">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SCSI \| ScsiPort")</span><span class="sxs-lookup"><span data-stu-id="202b2-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-333">Número de índice do controlador SCSI no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="202b2-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="202b2-334">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="202b2-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="202b2-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="202b2-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-336">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="202b2-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-338">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="202b2-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-339">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="202b2-339">Date and time the object was installed.</span></span> <span data-ttu-id="202b2-340">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="202b2-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="202b2-341">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="202b2-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-343">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="202b2-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-345">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="202b2-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="202b2-346">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-347">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="202b2-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-350">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| manufatura")</span><span class="sxs-lookup"><span data-stu-id="202b2-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-351">Nome do fabricante do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="202b2-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="202b2-352">Exemplo: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="202b2-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="202b2-353">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="202b2-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-354">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="202b2-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-356">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="202b2-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-357">Largura máxima dos dados (em bits) com suporte pelo controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="202b2-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="202b2-358">Essa propriedade é herdada do [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-359">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="202b2-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-360">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="202b2-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-362">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="202b2-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-363">Número máximo de entidades diretamente endereçáveis com suporte por este controlador.</span><span class="sxs-lookup"><span data-stu-id="202b2-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="202b2-364">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="202b2-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="202b2-365">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-366">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="202b2-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-367">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="202b2-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-369">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="202b2-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-370">Taxa máxima de transferência (em bits por segundo) suportada pelo controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="202b2-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="202b2-371">Essa propriedade é herdada do [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="202b2-372">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="202b2-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-376">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="202b2-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-377">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="202b2-377">Label by which the object is known.</span></span> <span data-ttu-id="202b2-378">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="202b2-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="202b2-379">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="202b2-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-383">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="202b2-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-384">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="202b2-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="202b2-385">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="202b2-386">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="202b2-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="202b2-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="202b2-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-388">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="202b2-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="202b2-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-390">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="202b2-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="202b2-391">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="202b2-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="202b2-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="202b2-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="202b2-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="202b2-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="202b2-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="202b2-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="202b2-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="202b2-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-396">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="202b2-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="202b2-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="202b2-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-398">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="202b2-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="202b2-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="202b2-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-400">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="202b2-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="202b2-401">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="202b2-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="202b2-402">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="202b2-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="202b2-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-404">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="202b2-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="202b2-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="202b2-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="202b2-406">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="202b2-406">Timed Power-On Supported</span></span>

<span data-ttu-id="202b2-407">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="202b2-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-408">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="202b2-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-409">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="202b2-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-411">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="202b2-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="202b2-412">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="202b2-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="202b2-413">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-414">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="202b2-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-415">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="202b2-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-417">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Controlador de armazenamento DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="202b2-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-418">Suporte do controlador SCSI para redundância ou proteção contra falhas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202b2-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="202b2-419">Essa propriedade é herdada do [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="202b2-420">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="202b2-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="202b2-421">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="202b2-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="202b2-422">**Desprotegido** (3)</span><span class="sxs-lookup"><span data-stu-id="202b2-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="202b2-423">**Protegido** (4)</span><span class="sxs-lookup"><span data-stu-id="202b2-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="202b2-424">**Protegido por meio do SCC (comando do controlador SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="202b2-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="202b2-425">**Protegido por meio do SCC-2 (comando do controlador SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="202b2-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-426">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="202b2-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-427">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="202b2-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-429">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="202b2-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-430">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="202b2-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="202b2-431">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="202b2-432">A lista a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="202b2-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="202b2-433">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="202b2-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="202b2-434">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="202b2-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="202b2-435">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="202b2-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="202b2-436">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="202b2-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="202b2-437">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="202b2-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="202b2-438">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="202b2-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="202b2-439">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="202b2-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="202b2-440">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="202b2-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="202b2-441">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="202b2-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="202b2-442">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="202b2-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="202b2-443">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="202b2-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="202b2-444">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="202b2-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="202b2-445">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="202b2-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="202b2-446">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="202b2-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="202b2-447">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="202b2-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="202b2-448">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="202b2-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="202b2-449">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="202b2-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="202b2-450">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="202b2-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="202b2-451">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="202b2-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="202b2-452">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="202b2-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="202b2-453">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="202b2-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="202b2-454">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="202b2-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="202b2-455">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="202b2-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="202b2-456">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="202b2-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="202b2-457">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="202b2-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="202b2-458">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="202b2-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="202b2-459">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="202b2-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="202b2-460">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="202b2-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="202b2-461">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="202b2-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="202b2-462">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="202b2-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="202b2-463">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="202b2-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="202b2-464">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="202b2-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="202b2-465">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="202b2-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="202b2-466">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="202b2-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="202b2-467">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="202b2-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="202b2-468">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="202b2-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="202b2-469">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="202b2-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="202b2-470">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="202b2-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="202b2-471">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="202b2-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="202b2-472">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="202b2-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="202b2-473">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="202b2-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="202b2-474">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="202b2-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="202b2-475">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="202b2-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="202b2-476">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="202b2-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="202b2-477">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="202b2-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="202b2-478">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="202b2-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="202b2-479">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="202b2-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-480">**Status**</span><span class="sxs-lookup"><span data-stu-id="202b2-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-483">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="202b2-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-484">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="202b2-484">Current status of the object.</span></span> <span data-ttu-id="202b2-485">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="202b2-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="202b2-486">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="202b2-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="202b2-487">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="202b2-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="202b2-488">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="202b2-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="202b2-489">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="202b2-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="202b2-490">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="202b2-491">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="202b2-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="202b2-492">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="202b2-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="202b2-493">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="202b2-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="202b2-494">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="202b2-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="202b2-495">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="202b2-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="202b2-496">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="202b2-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="202b2-497">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="202b2-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="202b2-498">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="202b2-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="202b2-499">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="202b2-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="202b2-500">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="202b2-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="202b2-501">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="202b2-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="202b2-502">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="202b2-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="202b2-503">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="202b2-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="202b2-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-505">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="202b2-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-506">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-507">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="202b2-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="202b2-508">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="202b2-508">State of the logical device.</span></span> <span data-ttu-id="202b2-509">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="202b2-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="202b2-510">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="202b2-511">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="202b2-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="202b2-512">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="202b2-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="202b2-513">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="202b2-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="202b2-514">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="202b2-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="202b2-515">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="202b2-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="202b2-516">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="202b2-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-517">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-518">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-519">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="202b2-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="202b2-520">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="202b2-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="202b2-521">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-522">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="202b2-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="202b2-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202b2-525">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="202b2-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="202b2-526">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="202b2-526">Name of the scoping system.</span></span>

<span data-ttu-id="202b2-527">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="202b2-528">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="202b2-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202b2-529">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="202b2-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="202b2-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="202b2-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202b2-531">Data e hora da última redefinição deste controlador.</span><span class="sxs-lookup"><span data-stu-id="202b2-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="202b2-532">Isso pode significar que o controlador estava desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="202b2-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="202b2-533">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="202b2-534">Comentários</span><span class="sxs-lookup"><span data-stu-id="202b2-534">Remarks</span></span>

<span data-ttu-id="202b2-535">A classe **Win32 \_ SCSIController** é derivada de [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="202b2-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="202b2-536">Requisitos</span><span class="sxs-lookup"><span data-stu-id="202b2-536">Requirements</span></span>



| <span data-ttu-id="202b2-537">Requisito</span><span class="sxs-lookup"><span data-stu-id="202b2-537">Requirement</span></span> | <span data-ttu-id="202b2-538">Valor</span><span class="sxs-lookup"><span data-stu-id="202b2-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="202b2-539">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="202b2-539">Minimum supported client</span></span><br/> | <span data-ttu-id="202b2-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="202b2-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="202b2-541">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="202b2-541">Minimum supported server</span></span><br/> | <span data-ttu-id="202b2-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="202b2-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="202b2-543">Namespace</span><span class="sxs-lookup"><span data-stu-id="202b2-543">Namespace</span></span><br/>                | <span data-ttu-id="202b2-544">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="202b2-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="202b2-545">MOF</span><span class="sxs-lookup"><span data-stu-id="202b2-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="202b2-546"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="202b2-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="202b2-547">DLL</span><span class="sxs-lookup"><span data-stu-id="202b2-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="202b2-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="202b2-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202b2-549">Confira também</span><span class="sxs-lookup"><span data-stu-id="202b2-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202b2-550">**\_SCSICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="202b2-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="202b2-551">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="202b2-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
