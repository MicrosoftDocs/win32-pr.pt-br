---
description: A \_ classe do controlador CIM é uma classe pai para agrupar dispositivos diversos relacionados ao controle. Os exemplos de controladores são controladores SCSI, controladores USB e controladores seriais.
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: Classe CIM_Controller (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164003"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="0c94c-104">Classe CIM_Controller (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0c94c-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0c94c-105">A classe do **\_ controlador CIM** é uma classe pai para agrupar dispositivos diversos relacionados ao controle.</span><span class="sxs-lookup"><span data-stu-id="0c94c-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="0c94c-106">Os exemplos de controladores são controladores SCSI, controladores USB e controladores seriais.</span><span class="sxs-lookup"><span data-stu-id="0c94c-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="0c94c-107">A classe de **\_ controlador CIM** é uma abstração de dispositivos com uma pilha de protocolo único, que existe principalmente para comunicação e controle ou redefinição de dispositivos downstream ([**CIM \_ ControlledBy**](cim-controlledby.md)).</span><span class="sxs-lookup"><span data-stu-id="0c94c-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c94c-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0c94c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0c94c-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0c94c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0c94c-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0c94c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0c94c-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0c94c-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c94c-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c94c-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
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
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="0c94c-113">Membros</span><span class="sxs-lookup"><span data-stu-id="0c94c-113">Members</span></span>

<span data-ttu-id="0c94c-114">A classe do **\_ controlador CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0c94c-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="0c94c-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c94c-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c94c-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0c94c-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c94c-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c94c-117">Methods</span></span>

<span data-ttu-id="0c94c-118">A classe do **\_ controlador CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0c94c-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="0c94c-119">Método</span><span class="sxs-lookup"><span data-stu-id="0c94c-119">Method</span></span>                                                                | <span data-ttu-id="0c94c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c94c-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c94c-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0c94c-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="0c94c-122">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0c94c-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="0c94c-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0c94c-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0c94c-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0c94c-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="0c94c-125">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0c94c-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0c94c-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0c94c-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0c94c-127">Properties</span></span>

<span data-ttu-id="0c94c-128">A classe do **\_ controlador CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0c94c-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c94c-129">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="0c94c-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c94c-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0c94c-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-133">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c94c-133">Availability and status of the device.</span></span>

<span data-ttu-id="0c94c-134">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c94c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c94c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c94c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0c94c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0c94c-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0c94c-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0c94c-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0c94c-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0c94c-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="0c94c-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0c94c-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="0c94c-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0c94c-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="0c94c-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0c94c-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="0c94c-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0c94c-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="0c94c-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0c94c-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="0c94c-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0c94c-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="0c94c-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0c94c-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="0c94c-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0c94c-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="0c94c-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-148">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0c94c-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0c94c-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="0c94c-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-150">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0c94c-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="0c94c-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-152">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0c94c-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0c94c-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="0c94c-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0c94c-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0c94c-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-155">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0c94c-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0c94c-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0c94c-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-157">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0c94c-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0c94c-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0c94c-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-159">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="0c94c-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0c94c-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="0c94c-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-161">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0c94c-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="0c94c-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-163">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="0c94c-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c94c-164">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0c94c-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-167">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0c94c-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-168">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0c94c-168">A short textual description of the object.</span></span>

<span data-ttu-id="0c94c-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0c94c-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c94c-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-173">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0c94c-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-174">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0c94c-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0c94c-175">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0c94c-176">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-176">**This device is working properly.**</span></span> <span data-ttu-id="0c94c-177"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="0c94c-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0c94c-178">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="0c94c-179">(1)</span><span class="sxs-lookup"><span data-stu-id="0c94c-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0c94c-180">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0c94c-181">(2)</span><span class="sxs-lookup"><span data-stu-id="0c94c-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0c94c-182">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0c94c-183">(3)</span><span class="sxs-lookup"><span data-stu-id="0c94c-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0c94c-184">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0c94c-185">(4)</span><span class="sxs-lookup"><span data-stu-id="0c94c-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0c94c-186">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0c94c-187">(5)</span><span class="sxs-lookup"><span data-stu-id="0c94c-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0c94c-188">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0c94c-189"> (6)</span><span class="sxs-lookup"><span data-stu-id="0c94c-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0c94c-190">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-190">**Cannot filter.**</span></span> <span data-ttu-id="0c94c-191">(7)</span><span class="sxs-lookup"><span data-stu-id="0c94c-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0c94c-192">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0c94c-193">(8)</span><span class="sxs-lookup"><span data-stu-id="0c94c-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0c94c-194">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0c94c-195">(9)</span><span class="sxs-lookup"><span data-stu-id="0c94c-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0c94c-196">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-196">**This device cannot start.**</span></span> <span data-ttu-id="0c94c-197">(10)</span><span class="sxs-lookup"><span data-stu-id="0c94c-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0c94c-198">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-198">**This device failed.**</span></span> <span data-ttu-id="0c94c-199">(11)</span><span class="sxs-lookup"><span data-stu-id="0c94c-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0c94c-200">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0c94c-201">12</span><span class="sxs-lookup"><span data-stu-id="0c94c-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0c94c-202">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0c94c-203">(13)</span><span class="sxs-lookup"><span data-stu-id="0c94c-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0c94c-204">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0c94c-205">(14)</span><span class="sxs-lookup"><span data-stu-id="0c94c-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0c94c-206">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0c94c-207">(15)</span><span class="sxs-lookup"><span data-stu-id="0c94c-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0c94c-208">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0c94c-209">(16)</span><span class="sxs-lookup"><span data-stu-id="0c94c-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0c94c-210">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0c94c-211">(17)</span><span class="sxs-lookup"><span data-stu-id="0c94c-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0c94c-212">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0c94c-213">(18)</span><span class="sxs-lookup"><span data-stu-id="0c94c-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0c94c-214">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="0c94c-215">(19)</span><span class="sxs-lookup"><span data-stu-id="0c94c-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0c94c-216">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="0c94c-217">(20)</span><span class="sxs-lookup"><span data-stu-id="0c94c-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0c94c-218">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0c94c-219">(21)</span><span class="sxs-lookup"><span data-stu-id="0c94c-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0c94c-220">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-220">**This device is disabled.**</span></span> <span data-ttu-id="0c94c-221">(22)</span><span class="sxs-lookup"><span data-stu-id="0c94c-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0c94c-222">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0c94c-223">(23)</span><span class="sxs-lookup"><span data-stu-id="0c94c-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0c94c-224">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0c94c-225">(24)</span><span class="sxs-lookup"><span data-stu-id="0c94c-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0c94c-226">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0c94c-227">(25)</span><span class="sxs-lookup"><span data-stu-id="0c94c-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0c94c-228">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0c94c-229">(26)</span><span class="sxs-lookup"><span data-stu-id="0c94c-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0c94c-230">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0c94c-231">(27)</span><span class="sxs-lookup"><span data-stu-id="0c94c-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0c94c-232">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0c94c-233">(28)</span><span class="sxs-lookup"><span data-stu-id="0c94c-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0c94c-234">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0c94c-235">(29)</span><span class="sxs-lookup"><span data-stu-id="0c94c-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0c94c-236">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0c94c-237">(30)</span><span class="sxs-lookup"><span data-stu-id="0c94c-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0c94c-238">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c94c-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0c94c-239">(31)</span><span class="sxs-lookup"><span data-stu-id="0c94c-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c94c-240">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0c94c-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-241">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0c94c-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-243">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0c94c-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-244">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0c94c-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0c94c-245">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-246">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c94c-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-249">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c94c-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-250">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0c94c-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0c94c-251">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0c94c-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0c94c-252">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-253">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0c94c-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-256">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0c94c-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-257">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0c94c-257">A textual description of the object.</span></span>

<span data-ttu-id="0c94c-258">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-259">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0c94c-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-262">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c94c-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-263">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0c94c-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0c94c-264">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-265">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0c94c-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-266">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0c94c-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-268">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="0c94c-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0c94c-269">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0c94c-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-273">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="0c94c-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0c94c-274">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0c94c-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-276">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c94c-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-278">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0c94c-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-279">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-279">Indicates when the object was installed.</span></span> <span data-ttu-id="0c94c-280">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0c94c-281">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-282">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0c94c-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c94c-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-285">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0c94c-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0c94c-286">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="0c94c-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-288">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c94c-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-290">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="0c94c-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-291">Número máximo de entidades diretamente endereçáveis com suporte por este controlador.</span><span class="sxs-lookup"><span data-stu-id="0c94c-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="0c94c-292">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-293">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0c94c-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-296">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0c94c-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-297">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0c94c-297">Label by which the object is known.</span></span> <span data-ttu-id="0c94c-298">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="0c94c-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0c94c-299">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0c94c-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-303">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0c94c-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-304">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0c94c-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0c94c-305">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0c94c-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="0c94c-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-307">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0c94c-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-308">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c94c-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-310">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0c94c-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="0c94c-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c94c-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0c94c-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-313">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="0c94c-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0c94c-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0c94c-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-315">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c94c-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0c94c-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0c94c-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-317">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="0c94c-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0c94c-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0c94c-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-319">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0c94c-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0c94c-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0c94c-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-321">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="0c94c-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0c94c-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="0c94c-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-323">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="0c94c-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="0c94c-324">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="0c94c-325">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0c94c-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0c94c-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="0c94c-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-327">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="0c94c-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0c94c-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="0c94c-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0c94c-329">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="0c94c-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c94c-330">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0c94c-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-331">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0c94c-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-333">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0c94c-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0c94c-334">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0c94c-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0c94c-335">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0c94c-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0c94c-336">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0c94c-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0c94c-337">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-338">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="0c94c-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-339">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c94c-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-341">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="0c94c-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-342">O protocolo usado pelo controlador para acessar os dispositivos ' controlados '.</span><span class="sxs-lookup"><span data-stu-id="0c94c-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c94c-343">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c94c-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c94c-344">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0c94c-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="0c94c-345">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="0c94c-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="0c94c-346">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="0c94c-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="0c94c-347">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="0c94c-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="0c94c-348">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="0c94c-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="0c94c-349">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="0c94c-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="0c94c-350">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="0c94c-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="0c94c-351">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="0c94c-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="0c94c-352">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="0c94c-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="0c94c-353">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="0c94c-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="0c94c-354">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="0c94c-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="0c94c-355">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="0c94c-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="0c94c-356">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="0c94c-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="0c94c-357">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="0c94c-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="0c94c-358">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="0c94c-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="0c94c-359">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="0c94c-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="0c94c-360">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="0c94c-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="0c94c-361">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="0c94c-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="0c94c-362">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="0c94c-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="0c94c-363">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="0c94c-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="0c94c-364">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="0c94c-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="0c94c-365">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="0c94c-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="0c94c-366">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="0c94c-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="0c94c-367">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="0c94c-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="0c94c-368">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="0c94c-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="0c94c-369">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="0c94c-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="0c94c-370">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="0c94c-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="0c94c-371">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="0c94c-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="0c94c-372">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="0c94c-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="0c94c-373">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="0c94c-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="0c94c-374">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="0c94c-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="0c94c-375">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="0c94c-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="0c94c-376">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="0c94c-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="0c94c-377">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="0c94c-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="0c94c-378">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="0c94c-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="0c94c-379">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="0c94c-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="0c94c-380">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="0c94c-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="0c94c-381">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="0c94c-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="0c94c-382">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="0c94c-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="0c94c-383">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="0c94c-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="0c94c-384">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="0c94c-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="0c94c-385">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="0c94c-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="0c94c-386">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="0c94c-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="0c94c-387">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="0c94c-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="0c94c-388">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="0c94c-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="0c94c-389">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="0c94c-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c94c-390">**Status**</span><span class="sxs-lookup"><span data-stu-id="0c94c-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-393">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0c94c-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-394">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0c94c-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="0c94c-395">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="0c94c-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0c94c-396">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="0c94c-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0c94c-397">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="0c94c-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0c94c-398">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="0c94c-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0c94c-399">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="0c94c-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0c94c-400">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="0c94c-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0c94c-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0c94c-402">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0c94c-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0c94c-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0c94c-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0c94c-404">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0c94c-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0c94c-405">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0c94c-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c94c-406">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0c94c-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0c94c-407">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0c94c-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0c94c-408">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0c94c-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0c94c-409">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0c94c-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0c94c-410">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0c94c-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0c94c-411">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0c94c-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0c94c-412">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0c94c-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0c94c-413">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0c94c-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0c94c-414">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0c94c-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c94c-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0c94c-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-416">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c94c-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-418">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="0c94c-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-419">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0c94c-419">State of the logical device.</span></span> <span data-ttu-id="0c94c-420">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="0c94c-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="0c94c-421">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c94c-422">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c94c-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c94c-423">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0c94c-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0c94c-424">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0c94c-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0c94c-425">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="0c94c-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0c94c-426">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="0c94c-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c94c-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c94c-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-430">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c94c-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-431">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0c94c-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="0c94c-432">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0c94c-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0c94c-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-436">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c94c-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-437">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0c94c-437">The scoping system's name.</span></span>

<span data-ttu-id="0c94c-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c94c-439">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="0c94c-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c94c-440">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c94c-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c94c-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c94c-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c94c-442">Data e hora da última redefinição do controlador (desligado ou reinicializado).</span><span class="sxs-lookup"><span data-stu-id="0c94c-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c94c-443">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c94c-443">Remarks</span></span>

<span data-ttu-id="0c94c-444">A classe do **\_ controlador CIM** é derivada [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0c94c-445">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0c94c-445">WMI does not implement this class.</span></span> <span data-ttu-id="0c94c-446">Para classes derivadas do **\_ controlador CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0c94c-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0c94c-447">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0c94c-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0c94c-448">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0c94c-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c94c-449">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c94c-449">Requirements</span></span>



| <span data-ttu-id="0c94c-450">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c94c-450">Requirement</span></span> | <span data-ttu-id="0c94c-451">Valor</span><span class="sxs-lookup"><span data-stu-id="0c94c-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c94c-452">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c94c-452">Minimum supported client</span></span><br/> | <span data-ttu-id="0c94c-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c94c-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c94c-454">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c94c-454">Minimum supported server</span></span><br/> | <span data-ttu-id="0c94c-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c94c-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c94c-456">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c94c-456">Namespace</span></span><br/>                | <span data-ttu-id="0c94c-457">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0c94c-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c94c-458">MOF</span><span class="sxs-lookup"><span data-stu-id="0c94c-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c94c-459"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c94c-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c94c-460">DLL</span><span class="sxs-lookup"><span data-stu-id="0c94c-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c94c-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c94c-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c94c-462">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c94c-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c94c-463">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0c94c-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

