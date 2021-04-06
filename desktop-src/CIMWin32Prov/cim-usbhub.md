---
description: A \_ classe CIM USBHub representa os recursos e o gerenciamento de um hub USB.
ms.assetid: 33618963-3053-4c01-992e-aa6d9774f84b
ms.tgt_platform: multiple
title: Classe CIM_USBHub
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub
- CIM_USBHub.Availability
- CIM_USBHub.Caption
- CIM_USBHub.ClassCode
- CIM_USBHub.ConfigManagerErrorCode
- CIM_USBHub.ConfigManagerUserConfig
- CIM_USBHub.CreationClassName
- CIM_USBHub.CurrentAlternateSettings
- CIM_USBHub.CurrentConfigValue
- CIM_USBHub.Description
- CIM_USBHub.DeviceID
- CIM_USBHub.ErrorCleared
- CIM_USBHub.ErrorDescription
- CIM_USBHub.GangSwitched
- CIM_USBHub.InstallDate
- CIM_USBHub.LastErrorCode
- CIM_USBHub.Name
- CIM_USBHub.NumberOfConfigs
- CIM_USBHub.NumberOfPorts
- CIM_USBHub.PNPDeviceID
- CIM_USBHub.PowerManagementCapabilities
- CIM_USBHub.PowerManagementSupported
- CIM_USBHub.ProtocolCode
- CIM_USBHub.Status
- CIM_USBHub.StatusInfo
- CIM_USBHub.SubclassCode
- CIM_USBHub.SystemCreationClassName
- CIM_USBHub.SystemName
- CIM_USBHub.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9213b155b069b4aa19f2cbe910c0614f511ff8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920134"
---
# <a name="cim_usbhub-class"></a><span data-ttu-id="9b7e7-103">\_Classe CIM USBHub</span><span class="sxs-lookup"><span data-stu-id="9b7e7-103">CIM\_USBHub class</span></span>

<span data-ttu-id="9b7e7-104">A classe **CIM \_ USBHub** representa os recursos e o gerenciamento de um hub USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-104">The **CIM\_USBHub** class represents the capabilities and management of a USB hub.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b7e7-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b7e7-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b7e7-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9b7e7-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b7e7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b7e7-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBHub : CIM_USBDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  boolean  GangSwitched;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  uint8    NumberOfPorts;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="9b7e7-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9b7e7-110">Members</span></span>

<span data-ttu-id="9b7e7-111">A classe **CIM \_ USBHub** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9b7e7-111">The **CIM\_USBHub** class has these types of members:</span></span>

-   [<span data-ttu-id="9b7e7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b7e7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9b7e7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9b7e7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9b7e7-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b7e7-114">Methods</span></span>

<span data-ttu-id="9b7e7-115">A classe **CIM \_ USBHub** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-115">The **CIM\_USBHub** class has these methods.</span></span>



| <span data-ttu-id="9b7e7-116">Método</span><span class="sxs-lookup"><span data-stu-id="9b7e7-116">Method</span></span>                                                            | <span data-ttu-id="9b7e7-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b7e7-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b7e7-118">**Getdescriptor**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbhub.md) | <span data-ttu-id="9b7e7-119">Retorna o descritor de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="9b7e7-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="9b7e7-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-121">**Reset**</span></span>](reset-method-in-class-cim-usbhub.md)                 | <span data-ttu-id="9b7e7-122">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="9b7e7-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9b7e7-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbhub.md) | <span data-ttu-id="9b7e7-125">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9b7e7-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9b7e7-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9b7e7-127">Properties</span></span>

<span data-ttu-id="9b7e7-128">A classe **CIM \_ USBHub** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-128">The **CIM\_USBHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b7e7-129">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-133">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-133">Availability and status of the device.</span></span>

<span data-ttu-id="9b7e7-134">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b7e7-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b7e7-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9b7e7-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-138">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="9b7e7-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9b7e7-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9b7e7-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9b7e7-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9b7e7-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="9b7e7-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9b7e7-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9b7e7-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b7e7-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9b7e7-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9b7e7-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9b7e7-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-149">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9b7e7-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-151">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9b7e7-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-153">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9b7e7-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9b7e7-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-156">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9b7e7-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-158">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9b7e7-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-160">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9b7e7-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-162">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9b7e7-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-164">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b7e7-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-168">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-169">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-169">Short textual description of the object.</span></span>

<span data-ttu-id="9b7e7-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-172">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-174">Código de classe USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-174">USB class code.</span></span>

<span data-ttu-id="9b7e7-175">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-175">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-176">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-176">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-179">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-179">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-180">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-180">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9b7e7-181">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-181">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9b7e7-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9b7e7-183"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-183">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-184">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-184">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9b7e7-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9b7e7-186">(1)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-186">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-187">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-187">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b7e7-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9b7e7-189">(2)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-189">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9b7e7-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9b7e7-191">(3)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-191">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-192">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-192">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9b7e7-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9b7e7-194">(4)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-194">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-195">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-195">Device is not working properly.</span></span> <span data-ttu-id="9b7e7-196">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-196">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9b7e7-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9b7e7-198">(5)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-198">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-199">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-199">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9b7e7-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9b7e7-201"> (6)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-201">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-202">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-202">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9b7e7-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9b7e7-204">(7)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-204">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9b7e7-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9b7e7-206">(8)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-206">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-207">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-207">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9b7e7-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9b7e7-209">(9)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-209">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-210">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-210">Device is not working properly.</span></span> <span data-ttu-id="9b7e7-211">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-211">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9b7e7-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9b7e7-213">(10)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-213">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-214">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-214">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9b7e7-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9b7e7-216">(11)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-217">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-217">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9b7e7-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9b7e7-219">12</span><span class="sxs-lookup"><span data-stu-id="9b7e7-219">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-220">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-220">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9b7e7-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9b7e7-222">(13)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-222">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-223">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-223">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9b7e7-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9b7e7-225">(14)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-225">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-226">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-226">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9b7e7-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9b7e7-228">(15)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-228">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-229">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-229">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9b7e7-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9b7e7-231">(16)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-231">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-232">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-232">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9b7e7-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9b7e7-234">(17)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-234">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-235">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-235">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b7e7-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9b7e7-237">(18)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-237">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-238">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-238">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9b7e7-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9b7e7-240">(19)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9b7e7-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9b7e7-242">(20)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-242">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-243">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-243">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9b7e7-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9b7e7-245">(21)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-245">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-246">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-246">System failure.</span></span> <span data-ttu-id="9b7e7-247">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-247">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9b7e7-248">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-248">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9b7e7-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9b7e7-250">(22)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-250">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-251">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-251">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9b7e7-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9b7e7-253">(23)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-253">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-254">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-254">System failure.</span></span> <span data-ttu-id="9b7e7-255">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-255">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9b7e7-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9b7e7-257">(24)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-257">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-258">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-258">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9b7e7-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9b7e7-260">(25)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-260">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-261">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9b7e7-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9b7e7-263">(26)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-263">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-264">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9b7e7-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9b7e7-266">(27)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-266">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-267">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-267">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9b7e7-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9b7e7-269">(28)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-269">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-270">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-270">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9b7e7-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9b7e7-272">(29)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-272">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-273">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-273">Device is disabled.</span></span> <span data-ttu-id="9b7e7-274">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-274">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9b7e7-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9b7e7-276">(30)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-277">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b7e7-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9b7e7-279">(31)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-280">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-280">Device is not working properly.</span></span> <span data-ttu-id="9b7e7-281">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-281">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b7e7-282">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-282">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-283">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-283">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-285">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-285">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-286">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-286">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9b7e7-287">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-291">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-292">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-292">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9b7e7-293">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-293">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9b7e7-294">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-295">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-295">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-296">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-296">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-298">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ UsbDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-298">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-299">Configurações de USB alternativas para cada interface na configuração selecionada no momento (indicada pela propriedade **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-299">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="9b7e7-300">Essa matriz tem uma entrada para cada interface na configuração.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-300">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="9b7e7-301">Se a propriedade **CurrentConfigValue** tiver um valor de 0 (zero), que indica que o dispositivo não está configurado, a matriz será indefinida.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-301">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="9b7e7-302">Para obter mais informações sobre como analisar essa cadeia de caracteres de octeto, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-302">For more information about parsing this octet string, see the USB specification.</span></span>

<span data-ttu-id="9b7e7-303">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-303">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-304">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-304">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-305">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-305">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-307">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ UsbDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-307">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-308">Configuração selecionada no momento para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-308">Configuration currently selected for the device.</span></span> <span data-ttu-id="9b7e7-309">Se esse valor for 0 (zero), o dispositivo não será configurado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-309">If this value is 0 (zero), the device is unconfigured.</span></span>

<span data-ttu-id="9b7e7-310">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-310">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-311">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-314">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-315">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-315">Textual description of the object.</span></span>

<span data-ttu-id="9b7e7-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-320">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-321">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9b7e7-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-324">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-326">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9b7e7-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-331">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9b7e7-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-333">**GangSwitched**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-333">**GangSwitched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-334">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-336">Se **for true**, a energia será alternada para todas as portas no Hub simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-336">If **TRUE**, power is switched to all ports on the hub simultaneously.</span></span> <span data-ttu-id="9b7e7-337">Se for **false**, a energia será alternada individualmente para cada porta.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-337">If **FALSE**, power is switched individually for each port.</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-339">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-341">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-342">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-342">Date and time the object was installed.</span></span> <span data-ttu-id="9b7e7-343">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9b7e7-344">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-346">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-348">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9b7e7-349">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-350">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-353">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-354">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-354">Label by which the object is known.</span></span> <span data-ttu-id="9b7e7-355">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9b7e7-356">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-357">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-357">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-358">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-358">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-360">Número de configurações de dispositivo definidas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-360">Number of device configurations that are defined for the device.</span></span>

<span data-ttu-id="9b7e7-361">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-361">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-362">**NumberOfPorts**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-362">**NumberOfPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-363">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-363">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-365">Número de portas downstream no Hub, incluindo aquelas inseridas no silício do Hub.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-365">Number of downstream ports on the hub, including those embedded in the hub's silicon.</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-366">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-366">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-369">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-369">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-370">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-370">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9b7e7-371">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9b7e7-371">Example: "\*PNP030b"</span></span>

<span data-ttu-id="9b7e7-372">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-373">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-373">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-374">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-374">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-376">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-376">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9b7e7-377">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b7e7-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9b7e7-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b7e7-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b7e7-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-382">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-382">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9b7e7-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-384">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-384">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9b7e7-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-386">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="9b7e7-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9b7e7-387">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-387">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9b7e7-388">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-388">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9b7e7-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-390">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-390">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9b7e7-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9b7e7-392">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b7e7-393">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-393">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-394">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-394">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-396">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-396">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9b7e7-397">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9b7e7-397">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9b7e7-398">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-398">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9b7e7-399">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9b7e7-399">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9b7e7-400">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-401">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-401">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-402">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-402">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-404">Código de protocolo USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-404">USB protocol code.</span></span>

<span data-ttu-id="9b7e7-405">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-405">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-406">**Status**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-407">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-409">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-409">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-410">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-410">Current status of the object.</span></span>

<span data-ttu-id="9b7e7-411">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9b7e7-412">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9b7e7-412">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9b7e7-413">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-413">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9b7e7-414">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-414">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b7e7-415">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-415">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b7e7-416">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-416">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9b7e7-417">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-417">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9b7e7-418">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-418">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9b7e7-419">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-419">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b7e7-420">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-420">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9b7e7-421">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-421">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9b7e7-422">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-422">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9b7e7-423">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-423">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9b7e7-424">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-424">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b7e7-425">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-425">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-426">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-428">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="9b7e7-428">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-429">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-429">State of the logical device.</span></span> <span data-ttu-id="9b7e7-430">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-430">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9b7e7-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b7e7-432">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-432">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b7e7-433">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-433">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b7e7-434">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-434">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b7e7-435">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-435">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9b7e7-436">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-436">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b7e7-437">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-437">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-438">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-438">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-440">Código de subclasse USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-440">USB subclass code.</span></span>

<span data-ttu-id="9b7e7-441">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-441">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-442">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-442">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-445">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-446">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-446">Scoping system's creation class name.</span></span>

<span data-ttu-id="9b7e7-447">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-448">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-448">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-449">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-451">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b7e7-451">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-452">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-452">Scoping system's name.</span></span>

<span data-ttu-id="9b7e7-453">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b7e7-454">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-454">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b7e7-455">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b7e7-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b7e7-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b7e7-457">Versão USB mais recente com suporte do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-457">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="9b7e7-458">Essa propriedade é expressa como um decimal codificado em binário (BCD), em que um ponto decimal é implícito entre o segundo e o terceiro dígitos.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-458">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="9b7e7-459">Por exemplo, um valor de 0x201 indica que a versão 2, 1 tem suporte.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-459">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

<span data-ttu-id="9b7e7-460">Essa propriedade é herdada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-460">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b7e7-461">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b7e7-461">Remarks</span></span>

<span data-ttu-id="9b7e7-462">A classe **CIM \_ USBHub** é derivada do [**CIM \_ UsbDevice**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-462">The **CIM\_USBHub** class is derived from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

<span data-ttu-id="9b7e7-463">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-463">WMI does not implement this class.</span></span> <span data-ttu-id="9b7e7-464">Para classes WMI derivadas de **CIM \_ USBHub**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9b7e7-464">For WMI classes derived from **CIM\_USBHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9b7e7-465">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-465">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b7e7-466">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9b7e7-466">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b7e7-467">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b7e7-467">Requirements</span></span>



| <span data-ttu-id="9b7e7-468">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b7e7-468">Requirement</span></span> | <span data-ttu-id="9b7e7-469">Valor</span><span class="sxs-lookup"><span data-stu-id="9b7e7-469">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7e7-470">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b7e7-470">Minimum supported client</span></span><br/> | <span data-ttu-id="9b7e7-471">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b7e7-471">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b7e7-472">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b7e7-472">Minimum supported server</span></span><br/> | <span data-ttu-id="9b7e7-473">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b7e7-473">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b7e7-474">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b7e7-474">Namespace</span></span><br/>                | <span data-ttu-id="9b7e7-475">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9b7e7-475">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b7e7-476">MOF</span><span class="sxs-lookup"><span data-stu-id="9b7e7-476">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b7e7-477"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b7e7-477"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b7e7-478">DLL</span><span class="sxs-lookup"><span data-stu-id="9b7e7-478">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b7e7-479"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b7e7-479"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b7e7-480">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b7e7-480">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b7e7-481">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9b7e7-481">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

