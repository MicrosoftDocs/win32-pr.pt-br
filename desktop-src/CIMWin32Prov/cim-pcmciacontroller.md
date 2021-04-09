---
description: A \_ classe CIM PCMCIAController representa os recursos e o gerenciamento de um controlador de PCMCIA (Associação Internacional de cartão de memória) do computador pessoal.
ms.assetid: 341cbc6c-dd25-4dea-bcce-cd4e3f4d5324
ms.tgt_platform: multiple
title: Classe CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController
- CIM_PCMCIAController.Availability
- CIM_PCMCIAController.Caption
- CIM_PCMCIAController.ConfigManagerErrorCode
- CIM_PCMCIAController.ConfigManagerUserConfig
- CIM_PCMCIAController.CreationClassName
- CIM_PCMCIAController.Description
- CIM_PCMCIAController.DeviceID
- CIM_PCMCIAController.ErrorCleared
- CIM_PCMCIAController.ErrorDescription
- CIM_PCMCIAController.InstallDate
- CIM_PCMCIAController.LastErrorCode
- CIM_PCMCIAController.Manufacturer
- CIM_PCMCIAController.MaxNumberControlled
- CIM_PCMCIAController.Name
- CIM_PCMCIAController.PNPDeviceID
- CIM_PCMCIAController.PowerManagementCapabilities
- CIM_PCMCIAController.PowerManagementSupported
- CIM_PCMCIAController.ProtocolSupported
- CIM_PCMCIAController.Status
- CIM_PCMCIAController.StatusInfo
- CIM_PCMCIAController.SystemCreationClassName
- CIM_PCMCIAController.SystemName
- CIM_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95d05e11dd0c439708c477e3ec776bc7a2c333d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089117"
---
# <a name="cim_pcmciacontroller-class"></a><span data-ttu-id="9e82c-103">\_Classe CIM PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="9e82c-103">CIM\_PCMCIAController class</span></span>

<span data-ttu-id="9e82c-104">A classe **CIM \_ PCMCIAController** representa os recursos e o gerenciamento de um controlador de PCMCIA (Associação Internacional de cartão de memória) do computador pessoal.</span><span class="sxs-lookup"><span data-stu-id="9e82c-104">The **CIM\_PCMCIAController** class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e82c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9e82c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e82c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9e82c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9e82c-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9e82c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9e82c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9e82c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e82c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e82c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PCMCIAController : cim_controller
{
  uint16   Availability;
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="9e82c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9e82c-110">Members</span></span>

<span data-ttu-id="9e82c-111">A classe **CIM \_ PCMCIAController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9e82c-111">The **CIM\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="9e82c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e82c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e82c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e82c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e82c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e82c-114">Methods</span></span>

<span data-ttu-id="9e82c-115">A classe **CIM \_ PCMCIAController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9e82c-115">The **CIM\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="9e82c-116">Método</span><span class="sxs-lookup"><span data-stu-id="9e82c-116">Method</span></span>                                                                      | <span data-ttu-id="9e82c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e82c-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e82c-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="9e82c-118">**Reset**</span></span>](reset-method-in-class-cim-pcmciacontroller.md)                 | <span data-ttu-id="9e82c-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e82c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="9e82c-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9e82c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9e82c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9e82c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcmciacontroller.md) | <span data-ttu-id="9e82c-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9e82c-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9e82c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9e82c-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e82c-124">Properties</span></span>

<span data-ttu-id="9e82c-125">A classe **CIM \_ PCMCIAController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e82c-125">The **CIM\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e82c-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="9e82c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e82c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9e82c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-130">Availability and status of the device.</span></span> <span data-ttu-id="9e82c-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e82c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e82c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-133">Outros.</span><span class="sxs-lookup"><span data-stu-id="9e82c-133">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e82c-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="9e82c-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-135">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-135">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9e82c-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9e82c-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-137">Energia completa ou em execução.</span><span class="sxs-lookup"><span data-stu-id="9e82c-137">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9e82c-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="9e82c-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-139">Aviso.</span><span class="sxs-lookup"><span data-stu-id="9e82c-139">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9e82c-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="9e82c-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-141">Testes.</span><span class="sxs-lookup"><span data-stu-id="9e82c-141">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9e82c-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="9e82c-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-143">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="9e82c-143">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9e82c-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="9e82c-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-145">Desligar.</span><span class="sxs-lookup"><span data-stu-id="9e82c-145">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9e82c-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="9e82c-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-147">Offline.</span><span class="sxs-lookup"><span data-stu-id="9e82c-147">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9e82c-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="9e82c-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-149">Fora de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e82c-149">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9e82c-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="9e82c-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-151">Degradado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-151">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9e82c-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="9e82c-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-153">Não instalado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-153">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9e82c-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="9e82c-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-155">Erro de instalação.</span><span class="sxs-lookup"><span data-stu-id="9e82c-155">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9e82c-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="9e82c-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-157">É conhecido que o dispositivo esteja em um modo de economia de energia, mas seu status exato nesse modo é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-157">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9e82c-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="9e82c-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-159">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-159">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9e82c-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="9e82c-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-161">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-161">Device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9e82c-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="9e82c-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-163">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="9e82c-163">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9e82c-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="9e82c-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-165">O dispositivo está em um estado de aviso e também em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="9e82c-165">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9e82c-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9e82c-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-167">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="9e82c-167">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9e82c-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="9e82c-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-169">Não está pronto.</span><span class="sxs-lookup"><span data-stu-id="9e82c-169">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9e82c-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="9e82c-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-171">Não configurado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-171">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9e82c-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="9e82c-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-173">O controlador PCMCIA não está disponível.</span><span class="sxs-lookup"><span data-stu-id="9e82c-173">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e82c-174">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9e82c-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-177">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9e82c-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-178">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9e82c-178">Short textual description of the object.</span></span>

<span data-ttu-id="9e82c-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9e82c-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e82c-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-183">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e82c-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-184">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e82c-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9e82c-185">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9e82c-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9e82c-187"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="9e82c-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-188">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9e82c-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9e82c-190">(1)</span><span class="sxs-lookup"><span data-stu-id="9e82c-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-191">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9e82c-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9e82c-193">(2)</span><span class="sxs-lookup"><span data-stu-id="9e82c-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9e82c-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9e82c-195">(3)</span><span class="sxs-lookup"><span data-stu-id="9e82c-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-196">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="9e82c-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9e82c-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9e82c-198">(4)</span><span class="sxs-lookup"><span data-stu-id="9e82c-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-199">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-199">Device is not working properly.</span></span> <span data-ttu-id="9e82c-200">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9e82c-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9e82c-202">(5)</span><span class="sxs-lookup"><span data-stu-id="9e82c-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-203">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="9e82c-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9e82c-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9e82c-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="9e82c-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-206">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9e82c-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9e82c-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9e82c-208">(7)</span><span class="sxs-lookup"><span data-stu-id="9e82c-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9e82c-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9e82c-210">(8)</span><span class="sxs-lookup"><span data-stu-id="9e82c-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-211">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9e82c-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9e82c-213">(9)</span><span class="sxs-lookup"><span data-stu-id="9e82c-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-214">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-214">Device is not working properly.</span></span> <span data-ttu-id="9e82c-215">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9e82c-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9e82c-217">(10)</span><span class="sxs-lookup"><span data-stu-id="9e82c-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-218">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9e82c-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9e82c-220">(11)</span><span class="sxs-lookup"><span data-stu-id="9e82c-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-221">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9e82c-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9e82c-223">12</span><span class="sxs-lookup"><span data-stu-id="9e82c-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-224">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="9e82c-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9e82c-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9e82c-226">(13)</span><span class="sxs-lookup"><span data-stu-id="9e82c-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-227">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9e82c-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9e82c-229">(14)</span><span class="sxs-lookup"><span data-stu-id="9e82c-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-230">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9e82c-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9e82c-232">(15)</span><span class="sxs-lookup"><span data-stu-id="9e82c-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-233">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="9e82c-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9e82c-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9e82c-235">(16)</span><span class="sxs-lookup"><span data-stu-id="9e82c-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-236">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="9e82c-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9e82c-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9e82c-238">(17)</span><span class="sxs-lookup"><span data-stu-id="9e82c-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-239">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9e82c-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9e82c-241">(18)</span><span class="sxs-lookup"><span data-stu-id="9e82c-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-242">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="9e82c-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9e82c-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9e82c-244">(19)</span><span class="sxs-lookup"><span data-stu-id="9e82c-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9e82c-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9e82c-246">(20)</span><span class="sxs-lookup"><span data-stu-id="9e82c-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-247">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9e82c-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9e82c-249">(21)</span><span class="sxs-lookup"><span data-stu-id="9e82c-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-250">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="9e82c-250">System failure.</span></span> <span data-ttu-id="9e82c-251">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="9e82c-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9e82c-252">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9e82c-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9e82c-254">(22)</span><span class="sxs-lookup"><span data-stu-id="9e82c-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-255">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9e82c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9e82c-257">(23)</span><span class="sxs-lookup"><span data-stu-id="9e82c-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-258">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="9e82c-258">System failure.</span></span> <span data-ttu-id="9e82c-259">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="9e82c-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9e82c-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9e82c-261">(24)</span><span class="sxs-lookup"><span data-stu-id="9e82c-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-262">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="9e82c-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9e82c-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9e82c-264">(25)</span><span class="sxs-lookup"><span data-stu-id="9e82c-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-265">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9e82c-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9e82c-267">(26)</span><span class="sxs-lookup"><span data-stu-id="9e82c-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-268">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9e82c-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9e82c-270">(27)</span><span class="sxs-lookup"><span data-stu-id="9e82c-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-271">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="9e82c-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9e82c-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9e82c-273">(28)</span><span class="sxs-lookup"><span data-stu-id="9e82c-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-274">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="9e82c-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9e82c-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9e82c-276">(29)</span><span class="sxs-lookup"><span data-stu-id="9e82c-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-277">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-277">Device is disabled.</span></span> <span data-ttu-id="9e82c-278">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="9e82c-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9e82c-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9e82c-280">(30)</span><span class="sxs-lookup"><span data-stu-id="9e82c-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-281">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="9e82c-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9e82c-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e82c-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9e82c-283">(31)</span><span class="sxs-lookup"><span data-stu-id="9e82c-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-284">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-284">Device is not working properly.</span></span> <span data-ttu-id="9e82c-285">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="9e82c-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e82c-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9e82c-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-287">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9e82c-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-289">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e82c-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-290">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9e82c-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9e82c-291">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e82c-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-295">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e82c-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-296">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="9e82c-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9e82c-297">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="9e82c-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9e82c-298">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-299">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9e82c-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-302">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="9e82c-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-303">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9e82c-303">Textual description of the object.</span></span>

<span data-ttu-id="9e82c-304">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9e82c-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-308">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e82c-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-309">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e82c-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9e82c-310">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9e82c-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9e82c-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-314">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="9e82c-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9e82c-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9e82c-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-319">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="9e82c-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9e82c-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9e82c-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-322">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e82c-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-324">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="9e82c-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-325">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-325">Date and time the object was installed.</span></span> <span data-ttu-id="9e82c-326">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9e82c-327">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9e82c-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-329">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e82c-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-331">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e82c-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9e82c-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-333">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="9e82c-333">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-336">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e82c-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-337">Nome do fabricante do controlador PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="9e82c-337">Name of the PCMCIA controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-338">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="9e82c-338">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-339">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e82c-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-341">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="9e82c-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-342">Número máximo de entidades diretamente endereçáveis com suporte pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="9e82c-342">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="9e82c-343">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-343">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="9e82c-344">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-344">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-345">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9e82c-345">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-348">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9e82c-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-349">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-349">Label by which the object is known.</span></span> <span data-ttu-id="9e82c-350">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="9e82c-350">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9e82c-351">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-351">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9e82c-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-355">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e82c-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-356">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e82c-356">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9e82c-357">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9e82c-358">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9e82c-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-359">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9e82c-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-360">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e82c-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-362">Recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e82c-362">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="9e82c-363">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e82c-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9e82c-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-365">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9e82c-365">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9e82c-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="9e82c-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-367">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="9e82c-367">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e82c-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9e82c-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-369">Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-369">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e82c-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9e82c-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-371">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9e82c-371">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9e82c-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9e82c-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-373">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="9e82c-373">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9e82c-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="9e82c-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-375">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="9e82c-375">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9e82c-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="9e82c-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-377">O método [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="9e82c-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9e82c-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="9e82c-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9e82c-379">O método [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="9e82c-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e82c-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9e82c-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-381">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9e82c-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-383">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="9e82c-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9e82c-384">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9e82c-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9e82c-385">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="9e82c-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9e82c-386">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9e82c-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9e82c-387">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-388">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="9e82c-388">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-389">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e82c-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-391">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="9e82c-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-392">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="9e82c-392">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="9e82c-393">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-393">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="9e82c-394">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="9e82c-394">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e82c-395">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e82c-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e82c-396">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="9e82c-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="9e82c-397">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="9e82c-397">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="9e82c-398">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="9e82c-398">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="9e82c-399">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="9e82c-399">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="9e82c-400">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="9e82c-400">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="9e82c-401">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="9e82c-401">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="9e82c-402">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="9e82c-402">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="9e82c-403">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="9e82c-403">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="9e82c-404">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="9e82c-404">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="9e82c-405">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="9e82c-405">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="9e82c-406">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="9e82c-406">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="9e82c-407">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="9e82c-407">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="9e82c-408">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="9e82c-408">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="9e82c-409">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="9e82c-409">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="9e82c-410">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="9e82c-410">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="9e82c-411">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="9e82c-411">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="9e82c-412">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="9e82c-412">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="9e82c-413">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="9e82c-413">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="9e82c-414">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="9e82c-414">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="9e82c-415">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="9e82c-415">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="9e82c-416">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="9e82c-416">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="9e82c-417">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="9e82c-417">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="9e82c-418">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="9e82c-418">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="9e82c-419">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="9e82c-419">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="9e82c-420">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="9e82c-420">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="9e82c-421">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="9e82c-421">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="9e82c-422">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="9e82c-422">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="9e82c-423">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="9e82c-423">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="9e82c-424">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="9e82c-424">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="9e82c-425">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="9e82c-425">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="9e82c-426">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="9e82c-426">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="9e82c-427">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="9e82c-427">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="9e82c-428">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="9e82c-428">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="9e82c-429">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="9e82c-429">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="9e82c-430">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="9e82c-430">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="9e82c-431">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="9e82c-431">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="9e82c-432">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="9e82c-432">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="9e82c-433">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="9e82c-433">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="9e82c-434">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="9e82c-434">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="9e82c-435">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="9e82c-435">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="9e82c-436">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="9e82c-436">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="9e82c-437">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="9e82c-437">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="9e82c-438">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="9e82c-438">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="9e82c-439">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="9e82c-439">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="9e82c-440">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="9e82c-440">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="9e82c-441">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="9e82c-441">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e82c-442">**Status**</span><span class="sxs-lookup"><span data-stu-id="9e82c-442">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-445">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9e82c-445">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-446">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9e82c-446">Current status of the object.</span></span> <span data-ttu-id="9e82c-447">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9e82c-448">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9e82c-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9e82c-449">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9e82c-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9e82c-450">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="9e82c-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9e82c-451">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9e82c-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e82c-452">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="9e82c-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9e82c-453">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9e82c-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9e82c-454">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="9e82c-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9e82c-455">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="9e82c-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9e82c-456">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="9e82c-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9e82c-457">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="9e82c-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9e82c-458">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9e82c-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9e82c-459">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="9e82c-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9e82c-460">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="9e82c-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e82c-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9e82c-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-462">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e82c-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-464">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="9e82c-464">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-465">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e82c-465">State of the logical device.</span></span> <span data-ttu-id="9e82c-466">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9e82c-467">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e82c-468">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e82c-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e82c-469">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="9e82c-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e82c-470">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9e82c-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e82c-471">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="9e82c-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9e82c-472">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="9e82c-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e82c-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e82c-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-476">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e82c-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-477">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-477">Scoping system's creation class name.</span></span>

<span data-ttu-id="9e82c-478">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9e82c-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-480">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9e82c-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-482">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e82c-482">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-483">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="9e82c-483">Scoping system's name.</span></span>

<span data-ttu-id="9e82c-484">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e82c-485">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="9e82c-485">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e82c-486">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e82c-486">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e82c-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e82c-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e82c-488">Data e hora em que o controlador foi redefinido pela última vez, o que significa que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="9e82c-488">Date and time this controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="9e82c-489">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-489">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e82c-490">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e82c-490">Remarks</span></span>

<span data-ttu-id="9e82c-491">A classe **CIM \_ PCMCIAController** é derivada do [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-491">The **CIM\_PCMCIAController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="9e82c-492">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9e82c-492">WMI does not implement this class.</span></span> <span data-ttu-id="9e82c-493">Para classes WMI que são derivadas do **CIM \_ PCMCIAController**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9e82c-493">For WMI classes that are derived from **CIM\_PCMCIAController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9e82c-494">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9e82c-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e82c-495">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9e82c-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e82c-496">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e82c-496">Requirements</span></span>



| <span data-ttu-id="9e82c-497">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e82c-497">Requirement</span></span> | <span data-ttu-id="9e82c-498">Valor</span><span class="sxs-lookup"><span data-stu-id="9e82c-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e82c-499">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e82c-499">Minimum supported client</span></span><br/> | <span data-ttu-id="9e82c-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e82c-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e82c-501">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e82c-501">Minimum supported server</span></span><br/> | <span data-ttu-id="9e82c-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e82c-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e82c-503">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e82c-503">Namespace</span></span><br/>                | <span data-ttu-id="9e82c-504">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9e82c-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e82c-505">MOF</span><span class="sxs-lookup"><span data-stu-id="9e82c-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e82c-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e82c-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e82c-507">DLL</span><span class="sxs-lookup"><span data-stu-id="9e82c-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e82c-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e82c-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e82c-509">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e82c-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e82c-510">**\_controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="9e82c-510">**cim\_controller**</span></span>](cim-controller.md)
</dt> </dl>

 

