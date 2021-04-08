---
description: A \_ classe CIM LogicalDevice representa uma entidade de hardware que pode ou não ser realizada em hardware físico.
ms.assetid: 4f3d38ff-8080-4b53-ae29-82b68558c550
ms.tgt_platform: multiple
title: Classe CIM_LogicalDevice (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.Caption
- CIM_LogicalDevice.Description
- CIM_LogicalDevice.InstallDate
- CIM_LogicalDevice.Name
- CIM_LogicalDevice.Status
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.ConfigManagerErrorCode
- CIM_LogicalDevice.ConfigManagerUserConfig
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.PNPDeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49974b966e1378350e8e5475ef14bb092b3aaea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089271"
---
# <a name="cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="f062e-103">Classe CIM_LogicalDevice (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f062e-103">CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f062e-104">A classe **CIM \_ LogicalDevice** representa uma entidade de hardware que pode ou não ser realizada em hardware físico.</span><span class="sxs-lookup"><span data-stu-id="f062e-104">The **CIM\_LogicalDevice** class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f062e-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f062e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f062e-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f062e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f062e-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f062e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f062e-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f062e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f062e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f062e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C529-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDevice : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f062e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f062e-110">Members</span></span>

<span data-ttu-id="f062e-111">A classe **CIM \_ LogicalDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f062e-111">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="f062e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f062e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f062e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f062e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f062e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f062e-114">Methods</span></span>

<span data-ttu-id="f062e-115">A classe **CIM \_ LogicalDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f062e-115">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="f062e-116">Método</span><span class="sxs-lookup"><span data-stu-id="f062e-116">Method</span></span>                                                                   | <span data-ttu-id="f062e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f062e-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f062e-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="f062e-118">**Reset**</span></span>](reset-method-in-class-cim-logicaldevice.md)                 | <span data-ttu-id="f062e-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="f062e-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f062e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f062e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f062e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md) | <span data-ttu-id="f062e-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="f062e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f062e-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f062e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f062e-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f062e-124">Properties</span></span>

<span data-ttu-id="f062e-125">A classe **CIM \_ LogicalDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f062e-125">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f062e-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="f062e-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f062e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f062e-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f062e-130">Availability and status of the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f062e-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f062e-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f062e-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="f062e-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f062e-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="f062e-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f062e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="f062e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f062e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="f062e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f062e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="f062e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f062e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="f062e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f062e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="f062e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f062e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="f062e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f062e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="f062e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f062e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="f062e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f062e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="f062e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f062e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="f062e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="f062e-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f062e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="f062e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="f062e-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f062e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="f062e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f062e-148">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f062e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="f062e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f062e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="f062e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="f062e-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f062e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="f062e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="f062e-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f062e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="f062e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="f062e-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f062e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="f062e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="f062e-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f062e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="f062e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="f062e-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f062e-160">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f062e-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-163">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f062e-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-164">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f062e-164">A short textual description of the object.</span></span>

<span data-ttu-id="f062e-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f062e-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f062e-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f062e-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-169">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f062e-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-170">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f062e-170">Win32 Configuration Manager error code.</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f062e-171">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="f062e-171">**This device is working properly.**</span></span> <span data-ttu-id="f062e-172"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="f062e-172">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f062e-173">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="f062e-173">**This device is not configured correctly.**</span></span> <span data-ttu-id="f062e-174">(1)</span><span class="sxs-lookup"><span data-stu-id="f062e-174">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f062e-175">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-175">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f062e-176">(2)</span><span class="sxs-lookup"><span data-stu-id="f062e-176">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f062e-177">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="f062e-177">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f062e-178">(3)</span><span class="sxs-lookup"><span data-stu-id="f062e-178">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f062e-179">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="f062e-179">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f062e-180">(4)</span><span class="sxs-lookup"><span data-stu-id="f062e-180">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f062e-181">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="f062e-181">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f062e-182">(5)</span><span class="sxs-lookup"><span data-stu-id="f062e-182">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f062e-183">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="f062e-183">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f062e-184"> (6)</span><span class="sxs-lookup"><span data-stu-id="f062e-184">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f062e-185">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="f062e-185">**Cannot filter.**</span></span> <span data-ttu-id="f062e-186">(7)</span><span class="sxs-lookup"><span data-stu-id="f062e-186">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f062e-187">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="f062e-187">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f062e-188">(8)</span><span class="sxs-lookup"><span data-stu-id="f062e-188">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f062e-189">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="f062e-189">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f062e-190">(9)</span><span class="sxs-lookup"><span data-stu-id="f062e-190">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f062e-191">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="f062e-191">**This device cannot start.**</span></span> <span data-ttu-id="f062e-192">(10)</span><span class="sxs-lookup"><span data-stu-id="f062e-192">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f062e-193">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="f062e-193">**This device failed.**</span></span> <span data-ttu-id="f062e-194">(11)</span><span class="sxs-lookup"><span data-stu-id="f062e-194">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f062e-195">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="f062e-195">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f062e-196">12</span><span class="sxs-lookup"><span data-stu-id="f062e-196">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f062e-197">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-197">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f062e-198">(13)</span><span class="sxs-lookup"><span data-stu-id="f062e-198">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f062e-199">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="f062e-199">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f062e-200">(14)</span><span class="sxs-lookup"><span data-stu-id="f062e-200">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f062e-201">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="f062e-201">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f062e-202">(15)</span><span class="sxs-lookup"><span data-stu-id="f062e-202">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f062e-203">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="f062e-203">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f062e-204">(16)</span><span class="sxs-lookup"><span data-stu-id="f062e-204">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f062e-205">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="f062e-205">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f062e-206">(17)</span><span class="sxs-lookup"><span data-stu-id="f062e-206">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f062e-207">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-207">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f062e-208">(18)</span><span class="sxs-lookup"><span data-stu-id="f062e-208">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f062e-209">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="f062e-209">**Failure using the VxD loader.**</span></span> <span data-ttu-id="f062e-210">(19)</span><span class="sxs-lookup"><span data-stu-id="f062e-210">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f062e-211">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="f062e-211">**Your registry might be corrupted.**</span></span> <span data-ttu-id="f062e-212">(20)</span><span class="sxs-lookup"><span data-stu-id="f062e-212">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f062e-213">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-213">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f062e-214">(21)</span><span class="sxs-lookup"><span data-stu-id="f062e-214">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f062e-215">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="f062e-215">**This device is disabled.**</span></span> <span data-ttu-id="f062e-216">(22)</span><span class="sxs-lookup"><span data-stu-id="f062e-216">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f062e-217">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="f062e-217">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f062e-218">(23)</span><span class="sxs-lookup"><span data-stu-id="f062e-218">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f062e-219">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="f062e-219">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f062e-220">(24)</span><span class="sxs-lookup"><span data-stu-id="f062e-220">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f062e-221">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-221">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f062e-222">(25)</span><span class="sxs-lookup"><span data-stu-id="f062e-222">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f062e-223">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-223">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f062e-224">(26)</span><span class="sxs-lookup"><span data-stu-id="f062e-224">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f062e-225">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="f062e-225">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f062e-226">(27)</span><span class="sxs-lookup"><span data-stu-id="f062e-226">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f062e-227">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="f062e-227">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f062e-228">(28)</span><span class="sxs-lookup"><span data-stu-id="f062e-228">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f062e-229">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="f062e-229">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f062e-230">(29)</span><span class="sxs-lookup"><span data-stu-id="f062e-230">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f062e-231">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="f062e-231">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f062e-232">(30)</span><span class="sxs-lookup"><span data-stu-id="f062e-232">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f062e-233">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f062e-233">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f062e-234">(31)</span><span class="sxs-lookup"><span data-stu-id="f062e-234">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f062e-235">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f062e-235">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-236">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f062e-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-238">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f062e-238">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-239">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f062e-239">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f062e-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-243">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f062e-243">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f062e-244">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="f062e-244">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f062e-245">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f062e-245">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-246">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f062e-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-249">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="f062e-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-250">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f062e-250">A textual description of the object.</span></span>

<span data-ttu-id="f062e-251">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f062e-252">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f062e-252">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-255">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f062e-255">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f062e-256">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-256">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-257">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f062e-257">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-258">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f062e-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f062e-260">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="f062e-260">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-261">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f062e-261">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f062e-264">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="f062e-264">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f062e-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-266">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f062e-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-268">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="f062e-268">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-269">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f062e-269">Indicates when the object was installed.</span></span> <span data-ttu-id="f062e-270">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="f062e-270">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f062e-271">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-271">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f062e-272">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f062e-272">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f062e-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f062e-275">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-275">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-276">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f062e-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-279">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f062e-279">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-280">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="f062e-280">Label by which the object is known.</span></span> <span data-ttu-id="f062e-281">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="f062e-281">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f062e-282">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f062e-283">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f062e-283">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-286">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f062e-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-287">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-287">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f062e-288">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f062e-288">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f062e-289">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f062e-289">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-290">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f062e-290">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f062e-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f062e-292">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-292">Indicates the specific power-related capabilities of the logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f062e-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f062e-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-294">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="f062e-294">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f062e-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="f062e-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-296">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f062e-296">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f062e-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="f062e-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-298">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="f062e-298">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f062e-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="f062e-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-300">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f062e-300">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f062e-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="f062e-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-302">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="f062e-302">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f062e-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="f062e-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-304">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="f062e-304">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="f062e-305">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="f062e-305">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f062e-306">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f062e-306">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f062e-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="f062e-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-308">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="f062e-308">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f062e-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="f062e-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f062e-310">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="f062e-310">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f062e-311">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f062e-311">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f062e-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f062e-314">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="f062e-314">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f062e-315">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f062e-315">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f062e-316">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="f062e-316">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f062e-317">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f062e-317">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-318">**Status**</span><span class="sxs-lookup"><span data-stu-id="f062e-318">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-321">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f062e-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-322">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f062e-322">String that indicates the current status of the object.</span></span> <span data-ttu-id="f062e-323">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="f062e-323">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f062e-324">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="f062e-324">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f062e-325">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="f062e-325">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f062e-326">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="f062e-326">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f062e-327">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="f062e-327">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f062e-328">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="f062e-328">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f062e-329">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f062e-330">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f062e-330">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f062e-331">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f062e-331">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f062e-332">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="f062e-332">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f062e-333">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f062e-333">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f062e-334">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f062e-334">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f062e-335">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f062e-335">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f062e-336">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f062e-336">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f062e-337">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="f062e-337">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f062e-338">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="f062e-338">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f062e-339">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f062e-339">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f062e-340">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f062e-340">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f062e-341">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="f062e-341">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f062e-342">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f062e-342">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f062e-343">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f062e-343">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f062e-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-346">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="f062e-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f062e-347">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-347">State of the logical device.</span></span> <span data-ttu-id="f062e-348">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="f062e-348">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f062e-349">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f062e-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f062e-350">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="f062e-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f062e-351">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="f062e-351">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f062e-352">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="f062e-352">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f062e-353">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="f062e-353">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f062e-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f062e-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-357">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f062e-357">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f062e-358">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="f062e-358">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f062e-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f062e-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f062e-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f062e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f062e-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f062e-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f062e-362">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f062e-362">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f062e-363">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="f062e-363">The scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f062e-364">Comentários</span><span class="sxs-lookup"><span data-stu-id="f062e-364">Remarks</span></span>

<span data-ttu-id="f062e-365">As características do dispositivo lógico que gerenciam a operação ou a configuração estão contidas no objeto de **\_ LogicalDevice CIM** , ou associada a ele.</span><span class="sxs-lookup"><span data-stu-id="f062e-365">Logical device characteristics that manage operation or configuration are contained in, or associated with, the **CIM\_LogicalDevice** object.</span></span> <span data-ttu-id="f062e-366">As propriedades operacionais da impressora, por exemplo, são tamanhos de papel com suporte ou erros detectados.</span><span class="sxs-lookup"><span data-stu-id="f062e-366">Printer operational properties, for example, are supported paper sizes or detected errors.</span></span> <span data-ttu-id="f062e-367">As propriedades de configuração de dispositivo de sensor, por exemplo, são configurações de limite.</span><span class="sxs-lookup"><span data-stu-id="f062e-367">Sensor device configuration properties, for example, are threshold settings.</span></span> <span data-ttu-id="f062e-368">Várias configurações podem existir para um dispositivo lógico e estão contidas nos objetos de [**\_ configuração CIM**](cim-setting.md) , que estão associados ao dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f062e-368">Various configurations can exist for a logical device and are contained in the [**CIM\_Setting**](cim-setting.md) objects, which are associated with the logical device.</span></span>

<span data-ttu-id="f062e-369">A classe **CIM \_ LogicalDevice** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-369">The **CIM\_LogicalDevice** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="f062e-370">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f062e-370">WMI does not implement this class.</span></span> <span data-ttu-id="f062e-371">Para classes derivadas do **\_ LogicalDevice CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-371">For classes derived from **CIM\_LogicalDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f062e-372">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f062e-372">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f062e-373">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f062e-373">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f062e-374">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f062e-374">Requirements</span></span>



| <span data-ttu-id="f062e-375">Requisito</span><span class="sxs-lookup"><span data-stu-id="f062e-375">Requirement</span></span> | <span data-ttu-id="f062e-376">Valor</span><span class="sxs-lookup"><span data-stu-id="f062e-376">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f062e-377">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f062e-377">Minimum supported client</span></span><br/> | <span data-ttu-id="f062e-378">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f062e-378">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f062e-379">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f062e-379">Minimum supported server</span></span><br/> | <span data-ttu-id="f062e-380">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f062e-380">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f062e-381">Namespace</span><span class="sxs-lookup"><span data-stu-id="f062e-381">Namespace</span></span><br/>                | <span data-ttu-id="f062e-382">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f062e-382">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f062e-383">MOF</span><span class="sxs-lookup"><span data-stu-id="f062e-383">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f062e-384"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f062e-384"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f062e-385">DLL</span><span class="sxs-lookup"><span data-stu-id="f062e-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f062e-386"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f062e-386"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f062e-387">Confira também</span><span class="sxs-lookup"><span data-stu-id="f062e-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f062e-388">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="f062e-388">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

