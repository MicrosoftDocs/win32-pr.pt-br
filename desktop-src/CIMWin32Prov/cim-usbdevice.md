---
description: A \_ classe CIM UsbDevice representa as características de gerenciamento de um dispositivo USB.
ms.assetid: 0ff39701-826a-434b-a628-0af586600a80
ms.tgt_platform: multiple
title: Classe CIM_USBDevice (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.Availability
- CIM_USBDevice.Caption
- CIM_USBDevice.ClassCode
- CIM_USBDevice.ConfigManagerErrorCode
- CIM_USBDevice.ConfigManagerUserConfig
- CIM_USBDevice.CreationClassName
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.Description
- CIM_USBDevice.DeviceID
- CIM_USBDevice.ErrorCleared
- CIM_USBDevice.ErrorDescription
- CIM_USBDevice.InstallDate
- CIM_USBDevice.LastErrorCode
- CIM_USBDevice.Name
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.PNPDeviceID
- CIM_USBDevice.PowerManagementCapabilities
- CIM_USBDevice.PowerManagementSupported
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.Status
- CIM_USBDevice.StatusInfo
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.SystemCreationClassName
- CIM_USBDevice.SystemName
- CIM_USBDevice.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21b927980716d4ee7ee2e22a352c5c3b34b363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088879"
---
# <a name="cim_usbdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="0cb92-103">Classe CIM_USBDevice (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0cb92-103">CIM_USBDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0cb92-104">A classe **CIM \_ UsbDevice** representa as características de gerenciamento de um dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-104">The **CIM\_USBDevice** class represents the management characteristics of a USB device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0cb92-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0cb92-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0cb92-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0cb92-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0cb92-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0cb92-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0cb92-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0cb92-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb92-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cb92-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBDevice : CIM_LogicalDevice
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
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
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

## <a name="members"></a><span data-ttu-id="0cb92-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0cb92-110">Members</span></span>

<span data-ttu-id="0cb92-111">A classe **CIM \_ UsbDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0cb92-111">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="0cb92-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0cb92-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0cb92-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0cb92-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0cb92-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0cb92-114">Methods</span></span>

<span data-ttu-id="0cb92-115">A classe **CIM \_ UsbDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0cb92-115">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="0cb92-116">Método</span><span class="sxs-lookup"><span data-stu-id="0cb92-116">Method</span></span>                                                               | <span data-ttu-id="0cb92-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cb92-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cb92-118">**Getdescriptor**</span><span class="sxs-lookup"><span data-stu-id="0cb92-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md) | <span data-ttu-id="0cb92-119">Retorna o descritor de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="0cb92-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0cb92-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="0cb92-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0cb92-121">**Reset**</span></span>](reset-method-in-class-cim-usbdevice.md)                 | <span data-ttu-id="0cb92-122">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0cb92-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="0cb92-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0cb92-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0cb92-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0cb92-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbdevice.md) | <span data-ttu-id="0cb92-125">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0cb92-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0cb92-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0cb92-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0cb92-127">Properties</span></span>

<span data-ttu-id="0cb92-128">A classe **CIM \_ UsbDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0cb92-128">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cb92-129">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="0cb92-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb92-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0cb92-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-133">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-133">Availability and status of the device.</span></span>

<span data-ttu-id="0cb92-134">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0cb92-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0cb92-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0cb92-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0cb92-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0cb92-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0cb92-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-138">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="0cb92-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0cb92-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0cb92-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0cb92-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="0cb92-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0cb92-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="0cb92-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0cb92-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="0cb92-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0cb92-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="0cb92-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0cb92-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="0cb92-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0cb92-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="0cb92-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0cb92-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="0cb92-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0cb92-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="0cb92-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0cb92-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="0cb92-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-149">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0cb92-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0cb92-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="0cb92-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-151">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0cb92-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="0cb92-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-153">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0cb92-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="0cb92-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0cb92-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0cb92-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-156">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0cb92-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0cb92-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0cb92-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-158">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0cb92-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0cb92-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0cb92-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-160">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="0cb92-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0cb92-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="0cb92-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-162">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0cb92-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="0cb92-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-164">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="0cb92-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0cb92-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0cb92-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-168">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0cb92-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-169">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0cb92-169">Short textual description of the object.</span></span>

<span data-ttu-id="0cb92-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="0cb92-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-172">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0cb92-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-174">Código de classe USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-174">USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0cb92-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0cb92-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-178">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0cb92-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-179">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0cb92-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0cb92-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0cb92-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0cb92-182"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="0cb92-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-183">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0cb92-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0cb92-185">(1)</span><span class="sxs-lookup"><span data-stu-id="0cb92-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-186">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0cb92-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0cb92-188">(2)</span><span class="sxs-lookup"><span data-stu-id="0cb92-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0cb92-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0cb92-190">(3)</span><span class="sxs-lookup"><span data-stu-id="0cb92-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-191">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="0cb92-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0cb92-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0cb92-193">(4)</span><span class="sxs-lookup"><span data-stu-id="0cb92-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-194">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-194">Device is not working properly.</span></span> <span data-ttu-id="0cb92-195">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0cb92-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0cb92-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0cb92-197">(5)</span><span class="sxs-lookup"><span data-stu-id="0cb92-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-198">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="0cb92-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0cb92-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0cb92-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="0cb92-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-201">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0cb92-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0cb92-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0cb92-203">(7)</span><span class="sxs-lookup"><span data-stu-id="0cb92-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0cb92-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0cb92-205">(8)</span><span class="sxs-lookup"><span data-stu-id="0cb92-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-206">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0cb92-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0cb92-208">(9)</span><span class="sxs-lookup"><span data-stu-id="0cb92-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-209">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-209">Device is not working properly.</span></span> <span data-ttu-id="0cb92-210">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0cb92-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0cb92-212">(10)</span><span class="sxs-lookup"><span data-stu-id="0cb92-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-213">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0cb92-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0cb92-215">(11)</span><span class="sxs-lookup"><span data-stu-id="0cb92-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-216">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0cb92-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0cb92-218">12</span><span class="sxs-lookup"><span data-stu-id="0cb92-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-219">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="0cb92-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0cb92-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0cb92-221">(13)</span><span class="sxs-lookup"><span data-stu-id="0cb92-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-222">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0cb92-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0cb92-224">(14)</span><span class="sxs-lookup"><span data-stu-id="0cb92-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-225">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0cb92-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0cb92-227">(15)</span><span class="sxs-lookup"><span data-stu-id="0cb92-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-228">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="0cb92-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0cb92-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0cb92-230">(16)</span><span class="sxs-lookup"><span data-stu-id="0cb92-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-231">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="0cb92-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0cb92-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0cb92-233">(17)</span><span class="sxs-lookup"><span data-stu-id="0cb92-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-234">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0cb92-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0cb92-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0cb92-236">(18)</span><span class="sxs-lookup"><span data-stu-id="0cb92-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-237">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="0cb92-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0cb92-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0cb92-239">(19)</span><span class="sxs-lookup"><span data-stu-id="0cb92-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0cb92-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0cb92-241">(20)</span><span class="sxs-lookup"><span data-stu-id="0cb92-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-242">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0cb92-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0cb92-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0cb92-244">(21)</span><span class="sxs-lookup"><span data-stu-id="0cb92-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-245">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb92-245">System failure.</span></span> <span data-ttu-id="0cb92-246">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0cb92-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0cb92-247">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0cb92-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0cb92-249">(22)</span><span class="sxs-lookup"><span data-stu-id="0cb92-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-250">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0cb92-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0cb92-252">(23)</span><span class="sxs-lookup"><span data-stu-id="0cb92-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-253">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb92-253">System failure.</span></span> <span data-ttu-id="0cb92-254">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0cb92-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0cb92-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0cb92-256">(24)</span><span class="sxs-lookup"><span data-stu-id="0cb92-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-257">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="0cb92-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0cb92-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0cb92-259">(25)</span><span class="sxs-lookup"><span data-stu-id="0cb92-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-260">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0cb92-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0cb92-262">(26)</span><span class="sxs-lookup"><span data-stu-id="0cb92-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-263">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0cb92-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0cb92-265">(27)</span><span class="sxs-lookup"><span data-stu-id="0cb92-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-266">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="0cb92-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0cb92-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0cb92-268">(28)</span><span class="sxs-lookup"><span data-stu-id="0cb92-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-269">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="0cb92-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0cb92-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0cb92-271">(29)</span><span class="sxs-lookup"><span data-stu-id="0cb92-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-272">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-272">Device is disabled.</span></span> <span data-ttu-id="0cb92-273">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="0cb92-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0cb92-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0cb92-275">(30)</span><span class="sxs-lookup"><span data-stu-id="0cb92-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-276">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="0cb92-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0cb92-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0cb92-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0cb92-278">(31)</span><span class="sxs-lookup"><span data-stu-id="0cb92-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-279">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-279">Device is not working properly.</span></span> <span data-ttu-id="0cb92-280">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="0cb92-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0cb92-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0cb92-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-282">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0cb92-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-284">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0cb92-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-285">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0cb92-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0cb92-286">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0cb92-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-290">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0cb92-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-291">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0cb92-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0cb92-292">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0cb92-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0cb92-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-294">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="0cb92-294">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-295">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="0cb92-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-297">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ UsbDevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="0cb92-297">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-298">Configurações de USB alternativas para cada interface na configuração selecionada no momento (indicada pela propriedade **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="0cb92-298">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="0cb92-299">Essa matriz tem uma entrada para cada interface na configuração.</span><span class="sxs-lookup"><span data-stu-id="0cb92-299">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="0cb92-300">Se a propriedade **CurrentConfigValue** tiver um valor de 0 (zero), que indica que o dispositivo não está configurado, a matriz será indefinida.</span><span class="sxs-lookup"><span data-stu-id="0cb92-300">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="0cb92-301">Para obter mais informações sobre como analisar essa cadeia de caracteres de octeto, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-301">For more information about parsing this octet string, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-302">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="0cb92-302">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-303">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0cb92-303">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-305">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ UsbDevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="0cb92-305">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-306">Configuração selecionada no momento para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-306">Configuration currently selected for the device.</span></span> <span data-ttu-id="0cb92-307">Se o valor for 0 (zero), o dispositivo não será configurado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-307">If the value is 0 (zero), the device is unconfigured.</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-308">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0cb92-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-311">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0cb92-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-312">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0cb92-312">Textual description of the object.</span></span>

<span data-ttu-id="0cb92-313">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0cb92-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-317">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0cb92-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-318">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0cb92-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0cb92-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0cb92-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-321">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0cb92-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-323">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="0cb92-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0cb92-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0cb92-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-328">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="0cb92-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0cb92-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0cb92-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-331">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0cb92-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0cb92-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-334">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-334">Date and time the object was installed.</span></span> <span data-ttu-id="0cb92-335">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0cb92-336">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0cb92-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-338">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0cb92-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-340">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0cb92-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0cb92-341">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-342">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0cb92-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-345">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0cb92-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-346">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0cb92-346">Label by which the object is known.</span></span> <span data-ttu-id="0cb92-347">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="0cb92-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0cb92-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-349">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="0cb92-349">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-350">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0cb92-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-352">Número de configurações de dispositivo definidas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-352">Number of device configurations that are defined for the device.</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-353">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0cb92-353">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-354">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-356">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0cb92-356">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-357">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0cb92-357">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="0cb92-358">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0cb92-359">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0cb92-359">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-360">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0cb92-360">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-361">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb92-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-363">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0cb92-363">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0cb92-364">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="0cb92-364">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0cb92-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0cb92-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0cb92-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0cb92-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0cb92-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0cb92-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0cb92-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0cb92-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-369">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0cb92-369">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0cb92-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0cb92-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-371">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="0cb92-371">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0cb92-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="0cb92-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-373">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb92-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0cb92-374">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-374">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0cb92-375">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0cb92-375">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0cb92-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="0cb92-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-377">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="0cb92-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0cb92-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="0cb92-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0cb92-379">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="0cb92-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0cb92-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0cb92-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-381">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0cb92-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-383">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0cb92-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0cb92-384">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0cb92-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0cb92-385">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0cb92-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0cb92-386">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0cb92-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="0cb92-387">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-388">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="0cb92-388">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-389">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0cb92-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-391">Código de protocolo USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-391">USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-392">**Status**</span><span class="sxs-lookup"><span data-stu-id="0cb92-392">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-393">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-395">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0cb92-395">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-396">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0cb92-396">Current status of the object.</span></span> <span data-ttu-id="0cb92-397">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-397">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0cb92-398">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0cb92-398">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0cb92-399">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0cb92-399">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0cb92-400">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0cb92-400">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0cb92-401">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0cb92-401">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0cb92-402">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0cb92-402">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0cb92-403">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0cb92-403">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0cb92-404">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0cb92-404">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0cb92-405">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0cb92-405">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0cb92-406">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0cb92-406">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0cb92-407">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0cb92-407">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0cb92-408">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0cb92-408">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0cb92-409">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0cb92-409">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0cb92-410">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0cb92-410">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0cb92-411">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0cb92-411">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-412">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb92-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-414">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="0cb92-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-415">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0cb92-415">State of the logical device.</span></span> <span data-ttu-id="0cb92-416">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="0cb92-416">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0cb92-417">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0cb92-418">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0cb92-418">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0cb92-419">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0cb92-419">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0cb92-420">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0cb92-420">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0cb92-421">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="0cb92-421">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0cb92-422">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="0cb92-422">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0cb92-423">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="0cb92-423">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-424">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0cb92-424">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-426">Código de subclasse USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-426">USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0cb92-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-430">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0cb92-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-431">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="0cb92-432">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0cb92-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb92-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-436">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0cb92-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-437">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0cb92-437">Scoping system's name.</span></span>

<span data-ttu-id="0cb92-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb92-439">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="0cb92-439">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb92-440">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0cb92-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0cb92-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb92-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb92-442">Versão USB mais recente com suporte do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="0cb92-442">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="0cb92-443">Essa propriedade é expressa como um decimal codificado em binário (BCD), em que um ponto decimal é implícito entre o segundo e o terceiro dígitos.</span><span class="sxs-lookup"><span data-stu-id="0cb92-443">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="0cb92-444">Por exemplo, um valor de 0x201 indica que a versão 2, 1 tem suporte.</span><span class="sxs-lookup"><span data-stu-id="0cb92-444">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cb92-445">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb92-445">Remarks</span></span>

<span data-ttu-id="0cb92-446">A classe **CIM \_ UsbDevice** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-446">The **CIM\_USBDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0cb92-447">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0cb92-447">WMI does not implement this class.</span></span> <span data-ttu-id="0cb92-448">Para classes WMI que implementam **\_ UsbDevice CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0cb92-448">For WMI classes that implement **CIM\_USBDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0cb92-449">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0cb92-449">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0cb92-450">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0cb92-450">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb92-451">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb92-451">Requirements</span></span>



| <span data-ttu-id="0cb92-452">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb92-452">Requirement</span></span> | <span data-ttu-id="0cb92-453">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb92-453">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb92-454">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb92-454">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb92-455">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cb92-455">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cb92-456">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb92-456">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb92-457">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cb92-457">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cb92-458">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cb92-458">Namespace</span></span><br/>                | <span data-ttu-id="0cb92-459">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0cb92-459">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0cb92-460">MOF</span><span class="sxs-lookup"><span data-stu-id="0cb92-460">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cb92-461"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cb92-461"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cb92-462">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb92-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb92-463"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb92-463"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb92-464">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb92-464">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb92-465">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0cb92-465">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

