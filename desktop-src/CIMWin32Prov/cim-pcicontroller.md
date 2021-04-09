---
description: A \_ classe CIM PCIController representa as propriedades e o gerenciamento de um controlador PCI. As propriedades nessa classe e suas subclasses são definidas nas várias especificações de PCI publicadas pelo SIG de PCI.
ms.assetid: 0f2aec01-362d-49d7-95ea-23487214188c
ms.tgt_platform: multiple
title: Classe CIM_PCIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCIController
- CIM_PCIController.Availability
- CIM_PCIController.Caption
- CIM_PCIController.ConfigManagerErrorCode
- CIM_PCIController.ConfigManagerUserConfig
- CIM_PCIController.CreationClassName
- CIM_PCIController.Description
- CIM_PCIController.DeviceID
- CIM_PCIController.ErrorCleared
- CIM_PCIController.ErrorDescription
- CIM_PCIController.InstallDate
- CIM_PCIController.LastErrorCode
- CIM_PCIController.MaxNumberControlled
- CIM_PCIController.Name
- CIM_PCIController.PNPDeviceID
- CIM_PCIController.PowerManagementCapabilities
- CIM_PCIController.PowerManagementSupported
- CIM_PCIController.ProtocolSupported
- CIM_PCIController.Status
- CIM_PCIController.StatusInfo
- CIM_PCIController.SystemCreationClassName
- CIM_PCIController.SystemName
- CIM_PCIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4685f55899bf7b133a5039f40d77a2c6ca640d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089561"
---
# <a name="cim_pcicontroller-class"></a><span data-ttu-id="78849-104">\_Classe CIM PCIController</span><span class="sxs-lookup"><span data-stu-id="78849-104">CIM\_PCIController class</span></span>

<span data-ttu-id="78849-105">A classe **CIM \_ PCIController** representa as propriedades e o gerenciamento de um controlador PCI.</span><span class="sxs-lookup"><span data-stu-id="78849-105">The **CIM\_PCIController** class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="78849-106">As propriedades nessa classe e suas subclasses são definidas nas várias especificações de PCI publicadas pelo SIG de PCI.</span><span class="sxs-lookup"><span data-stu-id="78849-106">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78849-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="78849-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="78849-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="78849-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="78849-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="78849-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="78849-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="78849-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78849-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78849-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{7BB67AE8-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PCIController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="78849-112">Membros</span><span class="sxs-lookup"><span data-stu-id="78849-112">Members</span></span>

<span data-ttu-id="78849-113">A classe **CIM \_ PCIController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="78849-113">The **CIM\_PCIController** class has these types of members:</span></span>

-   [<span data-ttu-id="78849-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="78849-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="78849-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78849-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78849-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="78849-116">Methods</span></span>

<span data-ttu-id="78849-117">A classe **CIM \_ PCIController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="78849-117">The **CIM\_PCIController** class has these methods.</span></span>



| <span data-ttu-id="78849-118">Método</span><span class="sxs-lookup"><span data-stu-id="78849-118">Method</span></span>                                                                   | <span data-ttu-id="78849-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="78849-119">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78849-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="78849-120">**Reset**</span></span>](reset-method-in-class-cim-pcicontroller.md)                 | <span data-ttu-id="78849-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78849-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="78849-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="78849-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="78849-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="78849-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcicontroller.md) | <span data-ttu-id="78849-124">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="78849-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="78849-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="78849-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="78849-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78849-126">Properties</span></span>

<span data-ttu-id="78849-127">A classe **CIM \_ PCIController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="78849-127">The **CIM\_PCIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78849-128">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="78849-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78849-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78849-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="78849-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="78849-132">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-132">Availability and status of the device.</span></span> <span data-ttu-id="78849-133">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78849-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78849-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="78849-135">Outros.</span><span class="sxs-lookup"><span data-stu-id="78849-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78849-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78849-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="78849-137">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78849-137">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="78849-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="78849-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="78849-139">Energia completa ou em execução.</span><span class="sxs-lookup"><span data-stu-id="78849-139">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="78849-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="78849-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="78849-141">Aviso.</span><span class="sxs-lookup"><span data-stu-id="78849-141">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="78849-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="78849-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="78849-143">Testes.</span><span class="sxs-lookup"><span data-stu-id="78849-143">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="78849-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="78849-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="78849-145">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="78849-145">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="78849-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="78849-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="78849-147">Desligar.</span><span class="sxs-lookup"><span data-stu-id="78849-147">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="78849-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="78849-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="78849-149">Offline.</span><span class="sxs-lookup"><span data-stu-id="78849-149">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="78849-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="78849-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="78849-151">Fora de serviço.</span><span class="sxs-lookup"><span data-stu-id="78849-151">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78849-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="78849-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="78849-153">Degradado.</span><span class="sxs-lookup"><span data-stu-id="78849-153">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="78849-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="78849-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="78849-155">Não instalado.</span><span class="sxs-lookup"><span data-stu-id="78849-155">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="78849-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="78849-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="78849-157">Erro de instalação.</span><span class="sxs-lookup"><span data-stu-id="78849-157">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="78849-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="78849-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="78849-159">É conhecido que o dispositivo esteja em um modo de economia de energia, mas seu status exato nesse modo é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78849-159">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="78849-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="78849-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="78849-161">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="78849-161">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="78849-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="78849-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="78849-163">O dispositivo não está funcionando, mas pode ser levado para a potência completa ' rapidamente '.</span><span class="sxs-lookup"><span data-stu-id="78849-163">Device is not functioning, but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="78849-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="78849-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="78849-165">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="78849-165">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="78849-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="78849-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="78849-167">O dispositivo está em um estado de aviso e também em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="78849-167">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="78849-168"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="78849-168"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="78849-169">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="78849-169">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="78849-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="78849-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="78849-171">Não está pronto.</span><span class="sxs-lookup"><span data-stu-id="78849-171">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="78849-172"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="78849-172"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="78849-173">Não configurado.</span><span class="sxs-lookup"><span data-stu-id="78849-173">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="78849-174"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="78849-174"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="78849-175">O controlador PCI não está disponível.</span><span class="sxs-lookup"><span data-stu-id="78849-175">The PCI controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78849-176">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="78849-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-179">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="78849-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="78849-180">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="78849-180">Short textual description of the object.</span></span>

<span data-ttu-id="78849-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78849-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-182">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="78849-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78849-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78849-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-185">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="78849-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78849-186">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="78849-186">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="78849-187">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="78849-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="78849-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="78849-189"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="78849-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="78849-190">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78849-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="78849-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="78849-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="78849-192">(1)</span><span class="sxs-lookup"><span data-stu-id="78849-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="78849-193">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="78849-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78849-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="78849-195">(2)</span><span class="sxs-lookup"><span data-stu-id="78849-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="78849-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="78849-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="78849-197">(3)</span><span class="sxs-lookup"><span data-stu-id="78849-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="78849-198">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="78849-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="78849-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="78849-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="78849-200">(4)</span><span class="sxs-lookup"><span data-stu-id="78849-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="78849-201">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78849-201">Device is not working properly.</span></span> <span data-ttu-id="78849-202">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="78849-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="78849-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="78849-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="78849-204">(5)</span><span class="sxs-lookup"><span data-stu-id="78849-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="78849-205">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="78849-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="78849-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="78849-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="78849-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="78849-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="78849-208">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="78849-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="78849-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="78849-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="78849-210">(7)</span><span class="sxs-lookup"><span data-stu-id="78849-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="78849-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="78849-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="78849-212">(8)</span><span class="sxs-lookup"><span data-stu-id="78849-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="78849-213">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="78849-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="78849-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="78849-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="78849-215">(9)</span><span class="sxs-lookup"><span data-stu-id="78849-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="78849-216">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78849-216">Device is not working properly.</span></span> <span data-ttu-id="78849-217">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="78849-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="78849-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="78849-219">(10)</span><span class="sxs-lookup"><span data-stu-id="78849-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="78849-220">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="78849-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="78849-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="78849-222">(11)</span><span class="sxs-lookup"><span data-stu-id="78849-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="78849-223">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="78849-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="78849-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="78849-225">12</span><span class="sxs-lookup"><span data-stu-id="78849-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="78849-226">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="78849-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="78849-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="78849-228">(13)</span><span class="sxs-lookup"><span data-stu-id="78849-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="78849-229">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="78849-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="78849-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="78849-231">(14)</span><span class="sxs-lookup"><span data-stu-id="78849-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="78849-232">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="78849-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="78849-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="78849-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="78849-234">(15)</span><span class="sxs-lookup"><span data-stu-id="78849-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="78849-235">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="78849-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="78849-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="78849-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="78849-237">(16)</span><span class="sxs-lookup"><span data-stu-id="78849-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="78849-238">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="78849-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="78849-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="78849-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="78849-240">(17)</span><span class="sxs-lookup"><span data-stu-id="78849-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="78849-241">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78849-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78849-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="78849-243">(18)</span><span class="sxs-lookup"><span data-stu-id="78849-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="78849-244">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="78849-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="78849-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="78849-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="78849-246">(19)</span><span class="sxs-lookup"><span data-stu-id="78849-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="78849-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="78849-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="78849-248">(20)</span><span class="sxs-lookup"><span data-stu-id="78849-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="78849-249">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="78849-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="78849-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="78849-251">(21)</span><span class="sxs-lookup"><span data-stu-id="78849-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="78849-252">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="78849-252">System failure.</span></span> <span data-ttu-id="78849-253">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="78849-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="78849-254">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="78849-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="78849-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="78849-256">(22)</span><span class="sxs-lookup"><span data-stu-id="78849-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="78849-257">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="78849-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="78849-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="78849-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="78849-259">(23)</span><span class="sxs-lookup"><span data-stu-id="78849-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="78849-260">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="78849-260">System failure.</span></span> <span data-ttu-id="78849-261">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="78849-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="78849-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="78849-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="78849-263">(24)</span><span class="sxs-lookup"><span data-stu-id="78849-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="78849-264">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="78849-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="78849-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="78849-266">(25)</span><span class="sxs-lookup"><span data-stu-id="78849-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="78849-267">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="78849-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="78849-269">(26)</span><span class="sxs-lookup"><span data-stu-id="78849-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="78849-270">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78849-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="78849-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="78849-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="78849-272">(27)</span><span class="sxs-lookup"><span data-stu-id="78849-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="78849-273">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="78849-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="78849-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="78849-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="78849-275">(28)</span><span class="sxs-lookup"><span data-stu-id="78849-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="78849-276">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="78849-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="78849-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="78849-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="78849-278">(29)</span><span class="sxs-lookup"><span data-stu-id="78849-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="78849-279">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="78849-279">Device is disabled.</span></span> <span data-ttu-id="78849-280">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="78849-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="78849-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="78849-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="78849-282">(30)</span><span class="sxs-lookup"><span data-stu-id="78849-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="78849-283">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="78849-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78849-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78849-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="78849-285">(31)</span><span class="sxs-lookup"><span data-stu-id="78849-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="78849-286">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78849-286">Device is not working properly.</span></span> <span data-ttu-id="78849-287">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="78849-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78849-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="78849-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-289">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78849-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78849-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-291">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="78849-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78849-292">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="78849-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="78849-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78849-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-297">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78849-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78849-298">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="78849-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="78849-299">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="78849-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="78849-300">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-301">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="78849-301">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-304">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="78849-304">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="78849-305">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="78849-305">Textual description of the object.</span></span>

<span data-ttu-id="78849-306">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78849-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-307">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="78849-307">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-310">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78849-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78849-311">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78849-311">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="78849-312">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-313">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="78849-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-314">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78849-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78849-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78849-316">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="78849-316">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="78849-317">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="78849-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78849-321">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="78849-321">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="78849-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-323">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="78849-323">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-324">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78849-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78849-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-326">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="78849-326">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="78849-327">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="78849-327">Date and time the object was installed.</span></span> <span data-ttu-id="78849-328">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="78849-328">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="78849-329">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78849-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-330">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="78849-330">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78849-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78849-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78849-333">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78849-333">Last error code reported by the logical device.</span></span>

<span data-ttu-id="78849-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-335">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="78849-335">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-336">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78849-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78849-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-338">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="78849-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="78849-339">Número máximo de entidades diretamente endereçáveis com suporte pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="78849-339">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="78849-340">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="78849-340">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="78849-341">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78849-341">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-342">**Nome**</span><span class="sxs-lookup"><span data-stu-id="78849-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-345">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="78849-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="78849-346">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="78849-346">Label by which the object is known.</span></span> <span data-ttu-id="78849-347">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="78849-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="78849-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78849-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-349">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="78849-349">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-352">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="78849-352">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78849-353">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78849-353">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="78849-354">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="78849-355">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="78849-355">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="78849-356">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="78849-356">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-357">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78849-357">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="78849-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78849-359">Recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78849-359">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="78849-360">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78849-361"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="78849-361"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="78849-362">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78849-362">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="78849-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="78849-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="78849-364">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="78849-364">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="78849-365"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="78849-365"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="78849-366">Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="78849-366">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="78849-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="78849-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="78849-368">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="78849-368">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="78849-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="78849-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="78849-370">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="78849-370">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="78849-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="78849-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="78849-372">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="78849-372">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="78849-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="78849-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="78849-374">O método [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="78849-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="78849-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="78849-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="78849-376">O método [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="78849-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcicontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78849-377">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="78849-377">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-378">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78849-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78849-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78849-380">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="78849-380">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="78849-381">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="78849-381">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="78849-382">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="78849-382">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="78849-383">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="78849-383">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="78849-384">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-385">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="78849-385">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-386">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78849-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78849-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-388">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="78849-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="78849-389">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="78849-389">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="78849-390">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78849-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="78849-391">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="78849-391">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78849-392">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78849-392">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78849-393">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78849-393">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="78849-394">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="78849-394">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="78849-395">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="78849-395">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="78849-396">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="78849-396">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="78849-397">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="78849-397">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="78849-398">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="78849-398">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="78849-399">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="78849-399">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="78849-400">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="78849-400">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="78849-401">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="78849-401">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="78849-402">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="78849-402">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="78849-403">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="78849-403">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="78849-404">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="78849-404">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="78849-405">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="78849-405">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="78849-406">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="78849-406">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="78849-407">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="78849-407">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="78849-408">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="78849-408">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="78849-409">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="78849-409">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="78849-410">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="78849-410">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="78849-411">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="78849-411">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="78849-412">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="78849-412">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="78849-413">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="78849-413">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="78849-414">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="78849-414">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="78849-415">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="78849-415">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="78849-416">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="78849-416">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="78849-417">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="78849-417">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="78849-418">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="78849-418">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="78849-419">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="78849-419">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="78849-420">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="78849-420">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="78849-421">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="78849-421">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="78849-422">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="78849-422">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="78849-423">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="78849-423">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="78849-424">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="78849-424">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="78849-425">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="78849-425">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="78849-426">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="78849-426">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="78849-427">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="78849-427">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="78849-428">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="78849-428">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="78849-429">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="78849-429">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="78849-430">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="78849-430">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="78849-431">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="78849-431">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="78849-432">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="78849-432">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="78849-433">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="78849-433">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="78849-434">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="78849-434">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="78849-435">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="78849-435">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="78849-436">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="78849-436">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="78849-437">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="78849-437">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="78849-438">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="78849-438">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78849-439">**Status**</span><span class="sxs-lookup"><span data-stu-id="78849-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-442">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="78849-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="78849-443">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="78849-443">Current status of the object.</span></span> <span data-ttu-id="78849-444">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78849-444">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="78849-445">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="78849-445">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="78849-446">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="78849-446">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="78849-447">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="78849-447">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78849-448">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="78849-448">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78849-449">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="78849-449">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="78849-450">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="78849-450">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="78849-451">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="78849-451">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="78849-452">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="78849-452">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="78849-453">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="78849-453">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="78849-454">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="78849-454">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="78849-455">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="78849-455">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="78849-456">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="78849-456">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="78849-457">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="78849-457">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78849-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="78849-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-459">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78849-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78849-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-461">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="78849-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="78849-462">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78849-462">State of the logical device.</span></span> <span data-ttu-id="78849-463">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="78849-463">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="78849-464">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-464">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78849-465">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78849-465">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78849-466">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78849-466">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="78849-467">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="78849-467">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="78849-468">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="78849-468">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="78849-469">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="78849-469">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78849-470">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78849-470">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-471">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-473">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78849-473">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78849-474">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="78849-474">Scoping system's creation class name.</span></span>

<span data-ttu-id="78849-475">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-476">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="78849-476">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-477">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78849-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78849-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78849-479">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78849-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78849-480">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="78849-480">Scoping system's name.</span></span>

<span data-ttu-id="78849-481">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78849-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78849-482">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="78849-482">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78849-483">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78849-483">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78849-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78849-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78849-485">Data e hora da última redefinição do controlador, o que significa que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="78849-485">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="78849-486">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78849-486">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78849-487">Comentários</span><span class="sxs-lookup"><span data-stu-id="78849-487">Remarks</span></span>

<span data-ttu-id="78849-488">A classe **CIM \_ PCIController** é derivada do [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78849-488">The **CIM\_PCIController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="78849-489">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="78849-489">WMI does not implement this class.</span></span>

<span data-ttu-id="78849-490">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="78849-490">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="78849-491">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="78849-491">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="78849-492">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78849-492">Requirements</span></span>



| <span data-ttu-id="78849-493">Requisito</span><span class="sxs-lookup"><span data-stu-id="78849-493">Requirement</span></span> | <span data-ttu-id="78849-494">Valor</span><span class="sxs-lookup"><span data-stu-id="78849-494">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78849-495">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78849-495">Minimum supported client</span></span><br/> | <span data-ttu-id="78849-496">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78849-496">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78849-497">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78849-497">Minimum supported server</span></span><br/> | <span data-ttu-id="78849-498">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78849-498">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78849-499">Namespace</span><span class="sxs-lookup"><span data-stu-id="78849-499">Namespace</span></span><br/>                | <span data-ttu-id="78849-500">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="78849-500">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78849-501">MOF</span><span class="sxs-lookup"><span data-stu-id="78849-501">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78849-502"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78849-502"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78849-503">DLL</span><span class="sxs-lookup"><span data-stu-id="78849-503">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78849-504"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78849-504"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78849-505">Confira também</span><span class="sxs-lookup"><span data-stu-id="78849-505">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78849-506">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="78849-506">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

