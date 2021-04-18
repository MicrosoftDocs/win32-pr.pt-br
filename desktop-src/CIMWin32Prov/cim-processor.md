---
description: A \_ classe de processador CIM representa os recursos e o gerenciamento do dispositivo lógico do processador.
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: Classe CIM_Processor (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456944"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a><span data-ttu-id="284f9-103">Classe CIM_Processor (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="284f9-103">CIM_Processor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="284f9-104">A classe de **\_ processador CIM** representa os recursos e o gerenciamento do dispositivo lógico do processador.</span><span class="sxs-lookup"><span data-stu-id="284f9-104">The **CIM\_Processor** class represents the capabilities and management of the processor logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="284f9-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="284f9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="284f9-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="284f9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="284f9-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="284f9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="284f9-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="284f9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="284f9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="284f9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a><span data-ttu-id="284f9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="284f9-110">Members</span></span>

<span data-ttu-id="284f9-111">A classe de **\_ processador CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="284f9-111">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="284f9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="284f9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="284f9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="284f9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="284f9-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="284f9-114">Methods</span></span>

<span data-ttu-id="284f9-115">A classe de **\_ processador CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="284f9-115">The **CIM\_Processor** class has these methods.</span></span>



| <span data-ttu-id="284f9-116">Método</span><span class="sxs-lookup"><span data-stu-id="284f9-116">Method</span></span>                                                               | <span data-ttu-id="284f9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="284f9-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="284f9-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="284f9-118">**Reset**</span></span>](reset-method-in-class-cim-processor.md)                 | <span data-ttu-id="284f9-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="284f9-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="284f9-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="284f9-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="284f9-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="284f9-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-processor.md) | <span data-ttu-id="284f9-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="284f9-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="284f9-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="284f9-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="284f9-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="284f9-124">Properties</span></span>

<span data-ttu-id="284f9-125">A classe de **\_ processador CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="284f9-125">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="284f9-126">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="284f9-126">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-129">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="284f9-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-130">Largura do endereço do processador, em bits.</span><span class="sxs-lookup"><span data-stu-id="284f9-130">Processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-131">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="284f9-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-134">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="284f9-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-135">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-135">Availability and status of the device.</span></span>

<span data-ttu-id="284f9-136">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="284f9-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="284f9-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284f9-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="284f9-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="284f9-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="284f9-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-140">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="284f9-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="284f9-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="284f9-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="284f9-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="284f9-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="284f9-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="284f9-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="284f9-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="284f9-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="284f9-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="284f9-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="284f9-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="284f9-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="284f9-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="284f9-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="284f9-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="284f9-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="284f9-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="284f9-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="284f9-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="284f9-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-151">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="284f9-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="284f9-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="284f9-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-153">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="284f9-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="284f9-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="284f9-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-155">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="284f9-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="284f9-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="284f9-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="284f9-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-158">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="284f9-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="284f9-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="284f9-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-160">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="284f9-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="284f9-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="284f9-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-162">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="284f9-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="284f9-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="284f9-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-164">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="284f9-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="284f9-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="284f9-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-166">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="284f9-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="284f9-167">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="284f9-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-170">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="284f9-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-171">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="284f9-171">Short textual description of the object.</span></span>

<span data-ttu-id="284f9-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="284f9-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-174">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284f9-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-176">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="284f9-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-177">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="284f9-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="284f9-178">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="284f9-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="284f9-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="284f9-180"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="284f9-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-181">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="284f9-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="284f9-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="284f9-183">(1)</span><span class="sxs-lookup"><span data-stu-id="284f9-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-184">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="284f9-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="284f9-186">(2)</span><span class="sxs-lookup"><span data-stu-id="284f9-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="284f9-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="284f9-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="284f9-188">(3)</span><span class="sxs-lookup"><span data-stu-id="284f9-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-189">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="284f9-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="284f9-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="284f9-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="284f9-191">(4)</span><span class="sxs-lookup"><span data-stu-id="284f9-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-192">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-192">Device is not working properly.</span></span> <span data-ttu-id="284f9-193">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="284f9-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="284f9-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="284f9-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="284f9-195">(5)</span><span class="sxs-lookup"><span data-stu-id="284f9-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-196">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="284f9-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="284f9-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="284f9-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="284f9-198"> (6)</span><span class="sxs-lookup"><span data-stu-id="284f9-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-199">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="284f9-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="284f9-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="284f9-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="284f9-201">(7)</span><span class="sxs-lookup"><span data-stu-id="284f9-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="284f9-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="284f9-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="284f9-203">(8)</span><span class="sxs-lookup"><span data-stu-id="284f9-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-204">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="284f9-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="284f9-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="284f9-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="284f9-206">(9)</span><span class="sxs-lookup"><span data-stu-id="284f9-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-207">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-207">Device is not working properly.</span></span> <span data-ttu-id="284f9-208">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="284f9-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="284f9-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="284f9-210">(10)</span><span class="sxs-lookup"><span data-stu-id="284f9-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-211">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="284f9-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="284f9-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="284f9-213">(11)</span><span class="sxs-lookup"><span data-stu-id="284f9-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-214">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="284f9-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="284f9-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="284f9-216">12</span><span class="sxs-lookup"><span data-stu-id="284f9-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-217">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="284f9-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="284f9-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="284f9-219">(13)</span><span class="sxs-lookup"><span data-stu-id="284f9-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-220">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="284f9-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="284f9-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="284f9-222">(14)</span><span class="sxs-lookup"><span data-stu-id="284f9-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-223">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="284f9-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="284f9-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="284f9-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="284f9-225">(15)</span><span class="sxs-lookup"><span data-stu-id="284f9-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-226">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="284f9-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="284f9-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="284f9-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="284f9-228">(16)</span><span class="sxs-lookup"><span data-stu-id="284f9-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-229">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="284f9-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="284f9-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="284f9-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="284f9-231">(17)</span><span class="sxs-lookup"><span data-stu-id="284f9-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-232">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="284f9-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="284f9-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="284f9-234">(18)</span><span class="sxs-lookup"><span data-stu-id="284f9-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-235">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="284f9-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="284f9-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="284f9-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="284f9-237">(19)</span><span class="sxs-lookup"><span data-stu-id="284f9-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="284f9-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="284f9-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="284f9-239">(20)</span><span class="sxs-lookup"><span data-stu-id="284f9-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-240">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="284f9-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="284f9-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="284f9-242">(21)</span><span class="sxs-lookup"><span data-stu-id="284f9-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-243">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="284f9-243">System failure.</span></span> <span data-ttu-id="284f9-244">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="284f9-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="284f9-245">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="284f9-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="284f9-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="284f9-247">(22)</span><span class="sxs-lookup"><span data-stu-id="284f9-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-248">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="284f9-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="284f9-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="284f9-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="284f9-250">(23)</span><span class="sxs-lookup"><span data-stu-id="284f9-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-251">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="284f9-251">System failure.</span></span> <span data-ttu-id="284f9-252">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="284f9-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="284f9-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="284f9-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="284f9-254">(24)</span><span class="sxs-lookup"><span data-stu-id="284f9-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-255">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="284f9-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="284f9-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="284f9-257">(25)</span><span class="sxs-lookup"><span data-stu-id="284f9-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-258">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="284f9-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="284f9-260">(26)</span><span class="sxs-lookup"><span data-stu-id="284f9-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-261">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284f9-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="284f9-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="284f9-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="284f9-263">(27)</span><span class="sxs-lookup"><span data-stu-id="284f9-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-264">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="284f9-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="284f9-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="284f9-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="284f9-266">(28)</span><span class="sxs-lookup"><span data-stu-id="284f9-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-267">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="284f9-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="284f9-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="284f9-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="284f9-269">(29)</span><span class="sxs-lookup"><span data-stu-id="284f9-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-270">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="284f9-270">Device is disabled.</span></span> <span data-ttu-id="284f9-271">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="284f9-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="284f9-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="284f9-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="284f9-273">(30)</span><span class="sxs-lookup"><span data-stu-id="284f9-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-274">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="284f9-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="284f9-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="284f9-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="284f9-276">(31)</span><span class="sxs-lookup"><span data-stu-id="284f9-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-277">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-277">Device is not working properly.</span></span> <span data-ttu-id="284f9-278">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="284f9-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="284f9-279">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="284f9-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-280">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="284f9-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-282">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="284f9-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-283">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="284f9-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="284f9-284">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="284f9-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-288">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="284f9-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="284f9-289">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="284f9-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="284f9-290">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="284f9-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="284f9-291">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-292">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="284f9-292">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-293">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284f9-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-295">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 6,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" megahertz ")</span><span class="sxs-lookup"><span data-stu-id="284f9-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-296">Velocidade atual (em megahertz) do processador.</span><span class="sxs-lookup"><span data-stu-id="284f9-296">Current speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-297">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="284f9-297">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-298">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-300">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="284f9-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-301">Largura dos dados do processador, em bits.</span><span class="sxs-lookup"><span data-stu-id="284f9-301">Processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-302">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="284f9-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-305">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="284f9-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-306">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="284f9-306">Textual description of the object.</span></span>

<span data-ttu-id="284f9-307">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="284f9-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-311">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="284f9-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="284f9-312">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="284f9-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="284f9-313">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="284f9-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-315">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="284f9-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-317">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="284f9-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="284f9-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="284f9-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-322">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="284f9-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="284f9-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-324">**Família**</span><span class="sxs-lookup"><span data-stu-id="284f9-324">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-325">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-327">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 14,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processador CIM**.**OtherFamilyDescription**")</span><span class="sxs-lookup"><span data-stu-id="284f9-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|014.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-328">Tipo de família de processador.</span><span class="sxs-lookup"><span data-stu-id="284f9-328">Processor family type.</span></span>

<span data-ttu-id="284f9-329">Essa propriedade é herdada **do \_ processador CIM**.</span><span class="sxs-lookup"><span data-stu-id="284f9-329">This property is inherited from **CIM\_Processor**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="284f9-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="284f9-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284f9-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="284f9-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="284f9-332"><span id="8086"></span>**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="284f9-332"><span id="8086"></span>**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="284f9-333"><span id="80286"></span>**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="284f9-333"><span id="80286"></span>**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="284f9-334"><span id="80386"></span>**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="284f9-334"><span id="80386"></span>**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="284f9-335"><span id="80486"></span>**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="284f9-335"><span id="80486"></span>**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="284f9-336"><span id="8087"></span>**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="284f9-336"><span id="8087"></span>**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="284f9-337"><span id="80287"></span>**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="284f9-337"><span id="80287"></span>**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="284f9-338"><span id="80387"></span>**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="284f9-338"><span id="80387"></span>**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="284f9-339"><span id="80487"></span>**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="284f9-339"><span id="80487"></span>**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="284f9-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Marca Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="284f9-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium(R) brand** (11)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-341">Marca Pentium</span><span class="sxs-lookup"><span data-stu-id="284f9-341">Pentium brand</span></span>

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="284f9-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) pro** (12)</span><span class="sxs-lookup"><span data-stu-id="284f9-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium(R) Pro** (12)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-343">Pentium Pro</span><span class="sxs-lookup"><span data-stu-id="284f9-343">Pentium Pro</span></span>

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="284f9-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="284f9-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium(R) II** (13)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-345">Pentium II</span><span class="sxs-lookup"><span data-stu-id="284f9-345">Pentium II</span></span>

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="284f9-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Processador Pentium (R) com tecnologia MMX (TM)** (14)</span><span class="sxs-lookup"><span data-stu-id="284f9-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-347">Processador Pentium com tecnologia MMX</span><span class="sxs-lookup"><span data-stu-id="284f9-347">Pentium processor with MMX technology</span></span>

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="284f9-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="284f9-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron(TM)** (15)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-349">Processador</span><span class="sxs-lookup"><span data-stu-id="284f9-349">Celeron</span></span>

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="284f9-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="284f9-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-351">Pentium II Xeon</span><span class="sxs-lookup"><span data-stu-id="284f9-351">Pentium II Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="284f9-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="284f9-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium(R) III** (17)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-353">Pentium III</span><span class="sxs-lookup"><span data-stu-id="284f9-353">Pentium III</span></span>

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="284f9-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**Família M1** (18)</span><span class="sxs-lookup"><span data-stu-id="284f9-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="284f9-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**Família m2** (19)</span><span class="sxs-lookup"><span data-stu-id="284f9-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="284f9-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**Família K5** (24)</span><span class="sxs-lookup"><span data-stu-id="284f9-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 Family** (24)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-357">Família de processadores AMD Duron</span><span class="sxs-lookup"><span data-stu-id="284f9-357">AMD Duron  Processor Family</span></span>

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="284f9-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**Família K6** (25)</span><span class="sxs-lookup"><span data-stu-id="284f9-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 Family** (25)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-359">Família K5</span><span class="sxs-lookup"><span data-stu-id="284f9-359">K5 Family</span></span>

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="284f9-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="284f9-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="284f9-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="284f9-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="284f9-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**Família de processadores AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="284f9-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-363">Família de processadores AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="284f9-363">AMD Athlon Processor Family</span></span>

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="284f9-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**Processador AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="284f9-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-365">Processador AMD Duron</span><span class="sxs-lookup"><span data-stu-id="284f9-365">AMD  Duron Processor</span></span>

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="284f9-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**Família AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="284f9-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 Family** (30)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-367">Família AMD2900</span><span class="sxs-lookup"><span data-stu-id="284f9-367">AMD2900 Family</span></span>

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="284f9-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="284f9-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="284f9-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Família Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="284f9-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="284f9-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="284f9-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="284f9-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="284f9-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="284f9-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="284f9-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="284f9-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="284f9-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="284f9-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="284f9-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="284f9-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**X704 do Power PC** (38)</span><span class="sxs-lookup"><span data-stu-id="284f9-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="284f9-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="284f9-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="284f9-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Família alfa** (48)</span><span class="sxs-lookup"><span data-stu-id="284f9-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="284f9-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alfa 21064** (49)</span><span class="sxs-lookup"><span data-stu-id="284f9-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="284f9-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alfa 21066** (50)</span><span class="sxs-lookup"><span data-stu-id="284f9-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="284f9-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alfa 21164** (51)</span><span class="sxs-lookup"><span data-stu-id="284f9-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="284f9-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**21164PC alfa** (52)</span><span class="sxs-lookup"><span data-stu-id="284f9-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="284f9-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**21164A alfa** (53)</span><span class="sxs-lookup"><span data-stu-id="284f9-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="284f9-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alfa 21264** (54)</span><span class="sxs-lookup"><span data-stu-id="284f9-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="284f9-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alfa 21364** (55)</span><span class="sxs-lookup"><span data-stu-id="284f9-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="284f9-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**Família MIPS** (64)</span><span class="sxs-lookup"><span data-stu-id="284f9-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="284f9-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span><span class="sxs-lookup"><span data-stu-id="284f9-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="284f9-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span><span class="sxs-lookup"><span data-stu-id="284f9-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="284f9-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span><span class="sxs-lookup"><span data-stu-id="284f9-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="284f9-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span><span class="sxs-lookup"><span data-stu-id="284f9-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="284f9-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span><span class="sxs-lookup"><span data-stu-id="284f9-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="284f9-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**Família SPARC** (80)</span><span class="sxs-lookup"><span data-stu-id="284f9-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="284f9-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**Supersparc** (81)</span><span class="sxs-lookup"><span data-stu-id="284f9-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="284f9-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**MICROSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="284f9-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="284f9-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**IIep de microsparc** (83)</span><span class="sxs-lookup"><span data-stu-id="284f9-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="284f9-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span><span class="sxs-lookup"><span data-stu-id="284f9-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="284f9-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**ULTRASPARC II** (85)</span><span class="sxs-lookup"><span data-stu-id="284f9-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="284f9-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (86)</span><span class="sxs-lookup"><span data-stu-id="284f9-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="284f9-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**ULTRASPARC III** (87)</span><span class="sxs-lookup"><span data-stu-id="284f9-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="284f9-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC iiii** (88)</span><span class="sxs-lookup"><span data-stu-id="284f9-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="284f9-400"><span id="68040"></span>**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="284f9-400"><span id="68040"></span>**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="284f9-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**família 68XXX** (97)</span><span class="sxs-lookup"><span data-stu-id="284f9-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="284f9-402"><span id="68000"></span>**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="284f9-402"><span id="68000"></span>**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="284f9-403"><span id="68010"></span>**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="284f9-403"><span id="68010"></span>**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="284f9-404"><span id="68020"></span>**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="284f9-404"><span id="68020"></span>**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="284f9-405"><span id="68030"></span>**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="284f9-405"><span id="68030"></span>**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="284f9-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Família Hobbit** (112)</span><span class="sxs-lookup"><span data-stu-id="284f9-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="284f9-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe (TM) TM5000 Family** (120)</span><span class="sxs-lookup"><span data-stu-id="284f9-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-408">Família Crusoe TM5000</span><span class="sxs-lookup"><span data-stu-id="284f9-408">Crusoe TM5000 Family</span></span>

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="284f9-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe (TM) TM3000 Family** (121)</span><span class="sxs-lookup"><span data-stu-id="284f9-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-410">Família Crusoe TM3000</span><span class="sxs-lookup"><span data-stu-id="284f9-410">Crusoe TM3000 Family</span></span>

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="284f9-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon (TM) TM8000 Family** (122)</span><span class="sxs-lookup"><span data-stu-id="284f9-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-412">Família Efficeon8000</span><span class="sxs-lookup"><span data-stu-id="284f9-412">Efficeon8000 Family</span></span>

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="284f9-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span><span class="sxs-lookup"><span data-stu-id="284f9-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="284f9-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Processador Itanium (TM)** (130)</span><span class="sxs-lookup"><span data-stu-id="284f9-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium(TM) Processor** (130)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-415">Processador Itanium</span><span class="sxs-lookup"><span data-stu-id="284f9-415">Itanium  Processor</span></span>

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="284f9-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**Família de processadores AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="284f9-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-417">AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="284f9-417">AMD Athlon</span></span> 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span data-ttu-id="284f9-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**Família AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="284f9-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD Opteron(TM) Family** (132)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-419">Família AMD Opteron</span><span class="sxs-lookup"><span data-stu-id="284f9-419">AMD Opteron  Family</span></span>

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="284f9-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**Família PA-RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="284f9-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="284f9-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="284f9-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="284f9-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="284f9-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="284f9-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="284f9-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="284f9-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="284f9-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="284f9-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="284f9-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="284f9-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="284f9-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="284f9-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**Família V30** (160)</span><span class="sxs-lookup"><span data-stu-id="284f9-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="284f9-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="284f9-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-429">Pentium III Xeon</span><span class="sxs-lookup"><span data-stu-id="284f9-429">Pentium III Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="284f9-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Processador Pentium (r) III com tecnologia Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="284f9-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-431">Processador Pentium III com a tecnologia Intel SpeedStep</span><span class="sxs-lookup"><span data-stu-id="284f9-431">Pentium III Processor with Intel SpeedStep Technology</span></span>

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="284f9-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="284f9-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium(R) 4** (178)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-433">Pentium 4</span><span class="sxs-lookup"><span data-stu-id="284f9-433">Pentium 4</span></span>

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="284f9-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="284f9-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-435">Intel Xeon</span><span class="sxs-lookup"><span data-stu-id="284f9-435">Intel Xeon</span></span>

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="284f9-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**Família AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="284f9-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="284f9-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Processador Intel (R) Xeon (TM) MP** (181)</span><span class="sxs-lookup"><span data-stu-id="284f9-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-438">Processador Intel Xeon MP</span><span class="sxs-lookup"><span data-stu-id="284f9-438">Intel Xeon Processor MP</span></span>

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span data-ttu-id="284f9-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**Família AMD AthlonXP (TM)** (182)</span><span class="sxs-lookup"><span data-stu-id="284f9-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP(TM) Family** (182)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-440">Família AMD AthlonXP</span><span class="sxs-lookup"><span data-stu-id="284f9-440">AMD AthlonXP Family</span></span>

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span data-ttu-id="284f9-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**Família AMD AthlonMP (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="284f9-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP(TM) Family** (183)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-442">Família AMD AthlonMP</span><span class="sxs-lookup"><span data-stu-id="284f9-442">AMD AthlonMP Family</span></span>

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="284f9-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="284f9-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-444">Intel Itanium 2</span><span class="sxs-lookup"><span data-stu-id="284f9-444">Intel Itanium 2</span></span>

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span data-ttu-id="284f9-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Processador Intel Pentium M** (185)</span><span class="sxs-lookup"><span data-stu-id="284f9-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M Processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="284f9-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="284f9-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span data-ttu-id="284f9-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**Família IBM390** (200)</span><span class="sxs-lookup"><span data-stu-id="284f9-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span data-ttu-id="284f9-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span><span class="sxs-lookup"><span data-stu-id="284f9-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span data-ttu-id="284f9-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span><span class="sxs-lookup"><span data-stu-id="284f9-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span data-ttu-id="284f9-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span><span class="sxs-lookup"><span data-stu-id="284f9-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span data-ttu-id="284f9-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/arquitetura base** (204)</span><span class="sxs-lookup"><span data-stu-id="284f9-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/Architecture base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="284f9-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="284f9-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="284f9-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span><span class="sxs-lookup"><span data-stu-id="284f9-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="284f9-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span><span class="sxs-lookup"><span data-stu-id="284f9-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="284f9-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="284f9-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="284f9-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="284f9-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="284f9-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span><span class="sxs-lookup"><span data-stu-id="284f9-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="284f9-458"><span id="6x86"></span><span id="6X86"></span>**6 x86** (300)</span><span class="sxs-lookup"><span data-stu-id="284f9-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="284f9-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span><span class="sxs-lookup"><span data-stu-id="284f9-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="284f9-460"><span id="MII"></span><span id="mii"></span>**MiI** (302)</span><span class="sxs-lookup"><span data-stu-id="284f9-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="284f9-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span><span class="sxs-lookup"><span data-stu-id="284f9-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="284f9-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="284f9-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="284f9-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Processador de vídeo** (500)</span><span class="sxs-lookup"><span data-stu-id="284f9-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Video Processor** (500)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="284f9-464">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="284f9-464">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-465">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="284f9-465">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-467">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="284f9-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-468">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="284f9-468">Date and time the object was installed.</span></span> <span data-ttu-id="284f9-469">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="284f9-469">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="284f9-470">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-470">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-471">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="284f9-471">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-472">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284f9-472">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-473">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-474">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="284f9-474">Last error code reported by the logical device.</span></span>

<span data-ttu-id="284f9-475">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-476">**Loadpercentual**</span><span class="sxs-lookup"><span data-stu-id="284f9-476">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-477">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-479">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrProcessorLoad "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" percent ")</span><span class="sxs-lookup"><span data-stu-id="284f9-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-480">Carregamento do processador, com média no último minuto, em uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="284f9-480">Loading of the processor, averaged over the last minute, in a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-481">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="284f9-481">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-482">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284f9-482">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-484">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 6,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" megahertz ")</span><span class="sxs-lookup"><span data-stu-id="284f9-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-485">Velocidade máxima (em megahertz) do processador.</span><span class="sxs-lookup"><span data-stu-id="284f9-485">Maximum speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-486">**Nome**</span><span class="sxs-lookup"><span data-stu-id="284f9-486">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-489">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="284f9-489">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-490">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="284f9-490">Label by which the object is known.</span></span> <span data-ttu-id="284f9-491">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="284f9-491">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="284f9-492">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-492">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-493">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="284f9-493">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-494">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-496">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processador CIM**.**Família**")</span><span class="sxs-lookup"><span data-stu-id="284f9-496">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-497">Descrição do tipo de família de processadores.</span><span class="sxs-lookup"><span data-stu-id="284f9-497">Description of the processor family type.</span></span> <span data-ttu-id="284f9-498">Essa propriedade é usada quando a propriedade **Family** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="284f9-498">This property is used when the **Family** property is set to 1 ("Other").</span></span> <span data-ttu-id="284f9-499">Essa cadeia de caracteres deve ser definida como NULL quando a propriedade **Family** for um valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="284f9-499">This string should be set to null when the **Family** property is a value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="284f9-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-501">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-502">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-503">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="284f9-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-504">Plug and Play identificador do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="284f9-504">Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="284f9-505">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="284f9-506">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="284f9-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="284f9-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="284f9-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-508">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="284f9-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-510">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="284f9-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="284f9-511">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="284f9-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284f9-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="284f9-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="284f9-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="284f9-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="284f9-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="284f9-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="284f9-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="284f9-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-516">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="284f9-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="284f9-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="284f9-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-518">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="284f9-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="284f9-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="284f9-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-520">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="284f9-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="284f9-521">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="284f9-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="284f9-522">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="284f9-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="284f9-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="284f9-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-524">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="284f9-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="284f9-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="284f9-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-526">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="284f9-526">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="284f9-527">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="284f9-527">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-528">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="284f9-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-529">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-530">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="284f9-530">If **True**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="284f9-531">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="284f9-531">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="284f9-532">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="284f9-532">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="284f9-533">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="284f9-533">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="284f9-534">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-534">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-535">**Função**</span><span class="sxs-lookup"><span data-stu-id="284f9-535">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-536">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-536">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-537">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-538">Cadeia de caracteres de forma livre que descreve a função do processador.</span><span class="sxs-lookup"><span data-stu-id="284f9-538">Free-form string that describes the role of the processor.</span></span> <span data-ttu-id="284f9-539">Por exemplo, "processador central" ou "processador matemático".</span><span class="sxs-lookup"><span data-stu-id="284f9-539">For example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="284f9-540">**Status**</span><span class="sxs-lookup"><span data-stu-id="284f9-540">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-541">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-543">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="284f9-543">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-544">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="284f9-544">Current status of the object.</span></span>

<span data-ttu-id="284f9-545">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-545">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="284f9-546">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="284f9-546">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="284f9-547">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="284f9-547">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="284f9-548">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="284f9-548">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="284f9-549">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="284f9-549">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284f9-550">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="284f9-550">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="284f9-551">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="284f9-551">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="284f9-552">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="284f9-552">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="284f9-553">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="284f9-553">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="284f9-554">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="284f9-554">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="284f9-555">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="284f9-555">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="284f9-556">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="284f9-556">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="284f9-557">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="284f9-557">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="284f9-558">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="284f9-558">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="284f9-559">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="284f9-559">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-560">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-560">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-561">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-562">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="284f9-562">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-563">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="284f9-563">State of the logical device.</span></span> <span data-ttu-id="284f9-564">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="284f9-564">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="284f9-565">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-565">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="284f9-566">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="284f9-566">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284f9-567">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="284f9-567">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="284f9-568">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="284f9-568">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="284f9-569">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="284f9-569">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="284f9-570">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="284f9-570">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="284f9-571">**Depuração**</span><span class="sxs-lookup"><span data-stu-id="284f9-571">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-572">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-572">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-573">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-573">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-574">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processador CIM**.**Família**")</span><span class="sxs-lookup"><span data-stu-id="284f9-574">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-575">Cadeia de caracteres de forma livre que indica o nível de revisão do processador na família de processadores.</span><span class="sxs-lookup"><span data-stu-id="284f9-575">Free-form string that indicates the revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-576">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="284f9-576">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-577">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-578">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-579">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="284f9-579">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="284f9-580">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="284f9-580">Scoping system's creation class name.</span></span>

<span data-ttu-id="284f9-581">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-581">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-582">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="284f9-582">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-583">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-584">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-585">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="284f9-585">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="284f9-586">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="284f9-586">Scoping system's name.</span></span>

<span data-ttu-id="284f9-587">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="284f9-588">**UniqueId**</span><span class="sxs-lookup"><span data-stu-id="284f9-588">**UniqueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="284f9-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-590">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-590">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="284f9-591">Identificador global exclusivo para o processador.</span><span class="sxs-lookup"><span data-stu-id="284f9-591">Globally unique identifier for the processor.</span></span> <span data-ttu-id="284f9-592">Esse identificador só pode ser exclusivo dentro de uma família de processadores.</span><span class="sxs-lookup"><span data-stu-id="284f9-592">This identifier can only be unique within a processor family.</span></span>

</dd> <dt>

<span data-ttu-id="284f9-593">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="284f9-593">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="284f9-594">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="284f9-594">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="284f9-595">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="284f9-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="284f9-596">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 6,7 ")</span><span class="sxs-lookup"><span data-stu-id="284f9-596">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.7")</span></span>
</dt> </dl>

<span data-ttu-id="284f9-597">Informações de soquete de CPU, que incluem dados sobre como atualizar o processador (se houver suporte para atualizações).</span><span class="sxs-lookup"><span data-stu-id="284f9-597">CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="284f9-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="284f9-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="284f9-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="284f9-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="284f9-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Placa-filha** (3)</span><span class="sxs-lookup"><span data-stu-id="284f9-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="284f9-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**Soquete ZIF** (4)</span><span class="sxs-lookup"><span data-stu-id="284f9-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="284f9-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Substituição/transportado de volta** (5)</span><span class="sxs-lookup"><span data-stu-id="284f9-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Replacement/Piggy Back** (5)</span></span>


</dt> <dd>

<span data-ttu-id="284f9-603">Substituição ou transportado de volta</span><span class="sxs-lookup"><span data-stu-id="284f9-603">Replacement or piggy back</span></span>

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="284f9-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (6)</span><span class="sxs-lookup"><span data-stu-id="284f9-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="284f9-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**Soquete LIF** (7)</span><span class="sxs-lookup"><span data-stu-id="284f9-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="284f9-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span><span class="sxs-lookup"><span data-stu-id="284f9-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="284f9-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span><span class="sxs-lookup"><span data-stu-id="284f9-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="284f9-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**soquete 370 PIN** (10)</span><span class="sxs-lookup"><span data-stu-id="284f9-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="284f9-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span><span class="sxs-lookup"><span data-stu-id="284f9-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="284f9-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span><span class="sxs-lookup"><span data-stu-id="284f9-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="284f9-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Soquete 423** (13)</span><span class="sxs-lookup"><span data-stu-id="284f9-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="284f9-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Soquete A (soquete 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="284f9-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="284f9-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Soquete 478** (15)</span><span class="sxs-lookup"><span data-stu-id="284f9-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="284f9-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Soquete 754** (16)</span><span class="sxs-lookup"><span data-stu-id="284f9-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="284f9-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Soquete 940** (17)</span><span class="sxs-lookup"><span data-stu-id="284f9-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="284f9-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Soquete 939** (18)</span><span class="sxs-lookup"><span data-stu-id="284f9-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span></span>


<span data-ttu-id="284f9-617"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="284f9-617"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="284f9-618">Comentários</span><span class="sxs-lookup"><span data-stu-id="284f9-618">Remarks</span></span>

<span data-ttu-id="284f9-619">A classe de **\_ processador CIM** é derivada [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-619">The **CIM\_Processor** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="284f9-620">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="284f9-620">WMI does not implement this class.</span></span> <span data-ttu-id="284f9-621">Para classes WMI derivadas do **\_ processador CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="284f9-621">For WMI classes derived from **CIM\_Processor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="284f9-622">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="284f9-622">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="284f9-623">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="284f9-623">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="284f9-624">Requisitos</span><span class="sxs-lookup"><span data-stu-id="284f9-624">Requirements</span></span>



| <span data-ttu-id="284f9-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="284f9-625">Requirement</span></span> | <span data-ttu-id="284f9-626">Valor</span><span class="sxs-lookup"><span data-stu-id="284f9-626">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="284f9-627">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="284f9-627">Minimum supported client</span></span><br/> | <span data-ttu-id="284f9-628">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="284f9-628">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="284f9-629">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="284f9-629">Minimum supported server</span></span><br/> | <span data-ttu-id="284f9-630">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="284f9-630">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="284f9-631">Namespace</span><span class="sxs-lookup"><span data-stu-id="284f9-631">Namespace</span></span><br/>                | <span data-ttu-id="284f9-632">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="284f9-632">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="284f9-633">MOF</span><span class="sxs-lookup"><span data-stu-id="284f9-633">MOF</span></span><br/>                      | <dl> <span data-ttu-id="284f9-634"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="284f9-634"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="284f9-635">DLL</span><span class="sxs-lookup"><span data-stu-id="284f9-635">DLL</span></span><br/>                      | <dl> <span data-ttu-id="284f9-636"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="284f9-636"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284f9-637">Confira também</span><span class="sxs-lookup"><span data-stu-id="284f9-637">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284f9-638">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="284f9-638">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

