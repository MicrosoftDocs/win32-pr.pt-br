---
description: A \_ classe CIM BinarySensor fornece uma saída booliana.
ms.assetid: 51396a51-78ea-4c49-8dcc-7fb815f334ae
ms.tgt_platform: multiple
title: Classe CIM_BinarySensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor
- CIM_BinarySensor.Caption
- CIM_BinarySensor.Description
- CIM_BinarySensor.InstallDate
- CIM_BinarySensor.Name
- CIM_BinarySensor.Status
- CIM_BinarySensor.Availability
- CIM_BinarySensor.ConfigManagerErrorCode
- CIM_BinarySensor.ConfigManagerUserConfig
- CIM_BinarySensor.CreationClassName
- CIM_BinarySensor.DeviceID
- CIM_BinarySensor.PowerManagementCapabilities
- CIM_BinarySensor.ErrorCleared
- CIM_BinarySensor.ErrorDescription
- CIM_BinarySensor.LastErrorCode
- CIM_BinarySensor.PNPDeviceID
- CIM_BinarySensor.PowerManagementSupported
- CIM_BinarySensor.StatusInfo
- CIM_BinarySensor.SystemCreationClassName
- CIM_BinarySensor.SystemName
- CIM_BinarySensor.CurrentReading
- CIM_BinarySensor.ExpectedReading
- CIM_BinarySensor.InterpretationOfFalse
- CIM_BinarySensor.InterpretationOfTrue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0d795f98473c09937571d415e34cf6fcb7f3486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754867"
---
# <a name="cim_binarysensor-class"></a><span data-ttu-id="81ca5-103">\_Classe CIM BinarySensor</span><span class="sxs-lookup"><span data-stu-id="81ca5-103">CIM\_BinarySensor class</span></span>

<span data-ttu-id="81ca5-104">A classe **CIM \_ BinarySensor** fornece uma saída booliana.</span><span class="sxs-lookup"><span data-stu-id="81ca5-104">The **CIM\_BinarySensor** class provides a Boolean output.</span></span> <span data-ttu-id="81ca5-105">As propriedades **CurrentState** e **PossibleStates** foram adicionadas para o sensor, tornando a **subclasse \_ BinarySensor CIM** não mais necessária, embora seja mantida para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="81ca5-105">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="81ca5-106">Um sensor binário pode ser criado instanciando-se um sensor com dois Estados possíveis.</span><span class="sxs-lookup"><span data-stu-id="81ca5-106">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81ca5-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="81ca5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81ca5-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81ca5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81ca5-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="81ca5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="81ca5-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="81ca5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ca5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81ca5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{11140D44-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_BinarySensor : CIM_Sensor
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
  boolean  CurrentReading;
  boolean  ExpectedReading;
  string   InterpretationOfFalse;
  string   InterpretationOfTrue;
};
```

## <a name="members"></a><span data-ttu-id="81ca5-112">Membros</span><span class="sxs-lookup"><span data-stu-id="81ca5-112">Members</span></span>

<span data-ttu-id="81ca5-113">A classe **CIM \_ BinarySensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81ca5-113">The **CIM\_BinarySensor** class has these types of members:</span></span>

-   [<span data-ttu-id="81ca5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="81ca5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="81ca5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81ca5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81ca5-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="81ca5-116">Methods</span></span>

<span data-ttu-id="81ca5-117">A classe **CIM \_ BinarySensor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="81ca5-117">The **CIM\_BinarySensor** class has these methods.</span></span>



| <span data-ttu-id="81ca5-118">Método</span><span class="sxs-lookup"><span data-stu-id="81ca5-118">Method</span></span>                                                                  | <span data-ttu-id="81ca5-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="81ca5-119">Description</span></span>                                                                                                                                |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81ca5-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="81ca5-120">**Reset**</span></span>](reset-method-in-class-cim-binarysensor.md)                 | <span data-ttu-id="81ca5-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81ca5-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="81ca5-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="81ca5-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="81ca5-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="81ca5-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-binarysensor.md) | <span data-ttu-id="81ca5-124">Define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="81ca5-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="81ca5-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81ca5-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81ca5-126">Properties</span></span>

<span data-ttu-id="81ca5-127">A classe **CIM \_ BinarySensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="81ca5-127">The **CIM\_BinarySensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81ca5-128">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="81ca5-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81ca5-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="81ca5-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-132">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81ca5-132">Availability and status of the device.</span></span>

<span data-ttu-id="81ca5-133">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81ca5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81ca5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81ca5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81ca5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="81ca5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="81ca5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="81ca5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="81ca5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="81ca5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="81ca5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81ca5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="81ca5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="81ca5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="81ca5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="81ca5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="81ca5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="81ca5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="81ca5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81ca5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="81ca5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="81ca5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="81ca5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="81ca5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="81ca5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="81ca5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="81ca5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-147">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="81ca5-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="81ca5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="81ca5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-149">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="81ca5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="81ca5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-151">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="81ca5-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="81ca5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="81ca5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="81ca5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="81ca5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-154">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="81ca5-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="81ca5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="81ca5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-156">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="81ca5-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="81ca5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="81ca5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-158">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="81ca5-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="81ca5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="81ca5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-160">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="81ca5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="81ca5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-162">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="81ca5-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81ca5-163">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="81ca5-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-166">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="81ca5-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-167">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="81ca5-167">A short textual description of the object.</span></span>

<span data-ttu-id="81ca5-168">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-169">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81ca5-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81ca5-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-172">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81ca5-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-173">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81ca5-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="81ca5-174">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="81ca5-175">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-175">**This device is working properly.**</span></span> <span data-ttu-id="81ca5-176"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="81ca5-176">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="81ca5-177">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-177">**This device is not configured correctly.**</span></span> <span data-ttu-id="81ca5-178">(1)</span><span class="sxs-lookup"><span data-stu-id="81ca5-178">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81ca5-179">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-179">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="81ca5-180">(2)</span><span class="sxs-lookup"><span data-stu-id="81ca5-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="81ca5-181">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-181">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="81ca5-182">(3)</span><span class="sxs-lookup"><span data-stu-id="81ca5-182">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="81ca5-183">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-183">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="81ca5-184">(4)</span><span class="sxs-lookup"><span data-stu-id="81ca5-184">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="81ca5-185">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-185">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="81ca5-186">(5)</span><span class="sxs-lookup"><span data-stu-id="81ca5-186">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="81ca5-187">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-187">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="81ca5-188"> (6)</span><span class="sxs-lookup"><span data-stu-id="81ca5-188">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="81ca5-189">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-189">**Cannot filter.**</span></span> <span data-ttu-id="81ca5-190">(7)</span><span class="sxs-lookup"><span data-stu-id="81ca5-190">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="81ca5-191">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-191">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="81ca5-192">(8)</span><span class="sxs-lookup"><span data-stu-id="81ca5-192">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="81ca5-193">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-193">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="81ca5-194">(9)</span><span class="sxs-lookup"><span data-stu-id="81ca5-194">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="81ca5-195">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-195">**This device cannot start.**</span></span> <span data-ttu-id="81ca5-196">(10)</span><span class="sxs-lookup"><span data-stu-id="81ca5-196">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="81ca5-197">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-197">**This device failed.**</span></span> <span data-ttu-id="81ca5-198">(11)</span><span class="sxs-lookup"><span data-stu-id="81ca5-198">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="81ca5-199">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-199">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="81ca5-200">12</span><span class="sxs-lookup"><span data-stu-id="81ca5-200">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="81ca5-201">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-201">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="81ca5-202">(13)</span><span class="sxs-lookup"><span data-stu-id="81ca5-202">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="81ca5-203">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-203">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="81ca5-204">(14)</span><span class="sxs-lookup"><span data-stu-id="81ca5-204">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="81ca5-205">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-205">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="81ca5-206">(15)</span><span class="sxs-lookup"><span data-stu-id="81ca5-206">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="81ca5-207">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-207">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="81ca5-208">(16)</span><span class="sxs-lookup"><span data-stu-id="81ca5-208">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="81ca5-209">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-209">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="81ca5-210">(17)</span><span class="sxs-lookup"><span data-stu-id="81ca5-210">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81ca5-211">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-211">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="81ca5-212">(18)</span><span class="sxs-lookup"><span data-stu-id="81ca5-212">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="81ca5-213">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-213">**Failure using the VxD loader.**</span></span> <span data-ttu-id="81ca5-214">(19)</span><span class="sxs-lookup"><span data-stu-id="81ca5-214">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="81ca5-215">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-215">**Your registry might be corrupted.**</span></span> <span data-ttu-id="81ca5-216">(20)</span><span class="sxs-lookup"><span data-stu-id="81ca5-216">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="81ca5-217">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-217">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="81ca5-218">(21)</span><span class="sxs-lookup"><span data-stu-id="81ca5-218">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="81ca5-219">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-219">**This device is disabled.**</span></span> <span data-ttu-id="81ca5-220">(22)</span><span class="sxs-lookup"><span data-stu-id="81ca5-220">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="81ca5-221">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-221">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="81ca5-222">(23)</span><span class="sxs-lookup"><span data-stu-id="81ca5-222">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="81ca5-223">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-223">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="81ca5-224">(24)</span><span class="sxs-lookup"><span data-stu-id="81ca5-224">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="81ca5-225">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-225">**Windows is still setting up this device.**</span></span> <span data-ttu-id="81ca5-226">(25)</span><span class="sxs-lookup"><span data-stu-id="81ca5-226">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="81ca5-227">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="81ca5-228">(26)</span><span class="sxs-lookup"><span data-stu-id="81ca5-228">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="81ca5-229">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-229">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="81ca5-230">(27)</span><span class="sxs-lookup"><span data-stu-id="81ca5-230">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="81ca5-231">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-231">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="81ca5-232">(28)</span><span class="sxs-lookup"><span data-stu-id="81ca5-232">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="81ca5-233">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-233">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="81ca5-234">(29)</span><span class="sxs-lookup"><span data-stu-id="81ca5-234">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="81ca5-235">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-235">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="81ca5-236">(30)</span><span class="sxs-lookup"><span data-stu-id="81ca5-236">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81ca5-237">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81ca5-237">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="81ca5-238">(31)</span><span class="sxs-lookup"><span data-stu-id="81ca5-238">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81ca5-239">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="81ca5-239">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-240">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81ca5-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-242">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81ca5-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-243">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="81ca5-243">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="81ca5-244">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-244">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-245">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81ca5-245">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-248">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81ca5-248">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-249">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="81ca5-249">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="81ca5-250">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="81ca5-250">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="81ca5-251">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-251">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-252">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="81ca5-252">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-253">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81ca5-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-255">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="81ca5-255">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-256">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="81ca5-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-259">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="81ca5-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-260">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="81ca5-260">A textual description of the object.</span></span>

<span data-ttu-id="81ca5-261">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="81ca5-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-265">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81ca5-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-266">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81ca5-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="81ca5-267">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-268">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="81ca5-268">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-269">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81ca5-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-271">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="81ca5-271">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="81ca5-272">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-273">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="81ca5-273">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-276">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="81ca5-276">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="81ca5-277">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-278">**ExpectedReading**</span><span class="sxs-lookup"><span data-stu-id="81ca5-278">**ExpectedReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-279">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81ca5-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-281">Valor ' normal ' do sensor.</span><span class="sxs-lookup"><span data-stu-id="81ca5-281">'Normal' value for the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81ca5-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-283">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81ca5-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-285">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="81ca5-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-286">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-286">Indicates when the object was installed.</span></span> <span data-ttu-id="81ca5-287">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-287">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="81ca5-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-289">**InterpretationOfFalse**</span><span class="sxs-lookup"><span data-stu-id="81ca5-289">**InterpretationOfFalse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-292">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="81ca5-292">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-293">Descrição de um valor ' false ' do sensor binário.</span><span class="sxs-lookup"><span data-stu-id="81ca5-293">Description of a 'False' value from the binary sensor.</span></span> <span data-ttu-id="81ca5-294">Essas informações podem ser exibidas para um usuário.</span><span class="sxs-lookup"><span data-stu-id="81ca5-294">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-295">**InterpretationOfTrue**</span><span class="sxs-lookup"><span data-stu-id="81ca5-295">**InterpretationOfTrue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-298">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="81ca5-298">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-299">Descrição de um valor ' true ' do sensor binário.</span><span class="sxs-lookup"><span data-stu-id="81ca5-299">Description of a 'True' value from the binary sensor.</span></span> <span data-ttu-id="81ca5-300">Essas informações podem ser exibidas para um usuário.</span><span class="sxs-lookup"><span data-stu-id="81ca5-300">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-301">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81ca5-301">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-302">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81ca5-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-304">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81ca5-304">Last error code reported by the logical device.</span></span>

<span data-ttu-id="81ca5-305">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-306">**Nome**</span><span class="sxs-lookup"><span data-stu-id="81ca5-306">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-309">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="81ca5-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-310">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="81ca5-310">Label by which the object is known.</span></span> <span data-ttu-id="81ca5-311">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="81ca5-311">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="81ca5-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-313">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="81ca5-313">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-316">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81ca5-316">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-317">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81ca5-317">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="81ca5-318">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="81ca5-318">Example: "\*PNP030b"</span></span>

<span data-ttu-id="81ca5-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-320">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81ca5-320">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-321">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81ca5-321">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-323">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81ca5-323">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="81ca5-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81ca5-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="81ca5-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-326">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="81ca5-326">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="81ca5-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="81ca5-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-328">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81ca5-328">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="81ca5-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="81ca5-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-330">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="81ca5-330">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="81ca5-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="81ca5-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-332">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="81ca5-332">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="81ca5-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="81ca5-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-334">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="81ca5-334">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="81ca5-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="81ca5-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-336">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="81ca5-336">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="81ca5-337">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-337">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="81ca5-338">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="81ca5-338">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="81ca5-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="81ca5-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-340">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="81ca5-340">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="81ca5-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="81ca5-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="81ca5-342">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="81ca5-342">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81ca5-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="81ca5-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-344">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81ca5-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-346">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="81ca5-346">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="81ca5-347">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="81ca5-347">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="81ca5-348">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="81ca5-348">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="81ca5-349">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="81ca5-349">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="81ca5-350">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-351">**Status**</span><span class="sxs-lookup"><span data-stu-id="81ca5-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-354">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="81ca5-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-355">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="81ca5-355">String that indicates the current status of the object.</span></span> <span data-ttu-id="81ca5-356">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="81ca5-356">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="81ca5-357">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="81ca5-357">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="81ca5-358">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="81ca5-358">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="81ca5-359">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="81ca5-359">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="81ca5-360">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="81ca5-360">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="81ca5-361">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="81ca5-361">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="81ca5-362">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="81ca5-363">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="81ca5-363">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="81ca5-364">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="81ca5-364">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="81ca5-365">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="81ca5-365">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81ca5-366">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="81ca5-366">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81ca5-367">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="81ca5-367">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="81ca5-368">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="81ca5-368">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="81ca5-369">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="81ca5-369">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="81ca5-370">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="81ca5-370">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="81ca5-371">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="81ca5-371">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="81ca5-372">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="81ca5-372">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="81ca5-373">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="81ca5-373">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="81ca5-374">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="81ca5-374">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="81ca5-375">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="81ca5-375">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81ca5-376">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="81ca5-376">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-377">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81ca5-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-379">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="81ca5-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-380">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81ca5-380">State of the logical device.</span></span> <span data-ttu-id="81ca5-381">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="81ca5-381">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="81ca5-382">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81ca5-383">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81ca5-383">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81ca5-384">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81ca5-384">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="81ca5-385">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="81ca5-385">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="81ca5-386">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="81ca5-386">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81ca5-387">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="81ca5-387">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81ca5-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81ca5-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-389">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-391">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81ca5-391">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-392">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="81ca5-392">The scoping system's creation class name.</span></span>

<span data-ttu-id="81ca5-393">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ca5-394">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="81ca5-394">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ca5-395">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81ca5-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81ca5-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ca5-397">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81ca5-397">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81ca5-398">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="81ca5-398">The scoping system's name.</span></span>

<span data-ttu-id="81ca5-399">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81ca5-400">Comentários</span><span class="sxs-lookup"><span data-stu-id="81ca5-400">Remarks</span></span>

<span data-ttu-id="81ca5-401">A classe **CIM \_ BinarySensor** é derivada do [**\_ sensor CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="81ca5-401">The **CIM\_BinarySensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="81ca5-402">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="81ca5-402">WMI does not implement this class.</span></span>

<span data-ttu-id="81ca5-403">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="81ca5-403">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81ca5-404">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="81ca5-404">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ca5-405">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ca5-405">Requirements</span></span>



| <span data-ttu-id="81ca5-406">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ca5-406">Requirement</span></span> | <span data-ttu-id="81ca5-407">Valor</span><span class="sxs-lookup"><span data-stu-id="81ca5-407">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81ca5-408">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81ca5-408">Minimum supported client</span></span><br/> | <span data-ttu-id="81ca5-409">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81ca5-409">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81ca5-410">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81ca5-410">Minimum supported server</span></span><br/> | <span data-ttu-id="81ca5-411">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81ca5-411">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81ca5-412">Namespace</span><span class="sxs-lookup"><span data-stu-id="81ca5-412">Namespace</span></span><br/>                | <span data-ttu-id="81ca5-413">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="81ca5-413">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81ca5-414">MOF</span><span class="sxs-lookup"><span data-stu-id="81ca5-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81ca5-415"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81ca5-415"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81ca5-416">DLL</span><span class="sxs-lookup"><span data-stu-id="81ca5-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ca5-417"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ca5-417"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ca5-418">Confira também</span><span class="sxs-lookup"><span data-stu-id="81ca5-418">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ca5-419">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="81ca5-419">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

