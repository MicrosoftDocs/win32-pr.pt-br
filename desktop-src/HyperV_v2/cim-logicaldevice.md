---
description: Uma abstração ou emulação de uma entidade de hardware que pode ou não ser baseada em hardware físico.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: Classe CIM_LogicalDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646688"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="dad07-103">Classe CIM_LogicalDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="dad07-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="dad07-104">Uma abstração ou emulação de uma entidade de hardware que pode ou não ser baseada em hardware físico.</span><span class="sxs-lookup"><span data-stu-id="dad07-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dad07-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="dad07-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dad07-106">Members</span></span>

<span data-ttu-id="dad07-107">A classe **CIM \_ LogicalDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dad07-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="dad07-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dad07-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="dad07-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dad07-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dad07-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dad07-110">Methods</span></span>

<span data-ttu-id="dad07-111">A classe **CIM \_ LogicalDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dad07-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="dad07-112">Método</span><span class="sxs-lookup"><span data-stu-id="dad07-112">Method</span></span>                                                           | <span data-ttu-id="dad07-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dad07-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dad07-114">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="dad07-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="dad07-115">Esse método é preterido.</span><span class="sxs-lookup"><span data-stu-id="dad07-115">This method is deprecated.</span></span> <span data-ttu-id="dad07-116">Em vez disso, use o método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dad07-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="dad07-117">**Descrição preterida:** Habilita ou desabilita o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="dad07-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="dad07-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="dad07-119">Esse método é preterido.</span><span class="sxs-lookup"><span data-stu-id="dad07-119">This method is deprecated.</span></span> <span data-ttu-id="dad07-120">Em vez disso, use o método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dad07-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="dad07-121">**Descrição preterida:** Coloca o dispositivo lógico online para que ele possa aceitar solicitações ou offline para que não possa mais aceitar solicitações.</span><span class="sxs-lookup"><span data-stu-id="dad07-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="dad07-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="dad07-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="dad07-123">Esse método é preterido.</span><span class="sxs-lookup"><span data-stu-id="dad07-123">This method is deprecated.</span></span> <span data-ttu-id="dad07-124">Em vez disso, use o método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dad07-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="dad07-125">**Descrição preterida:** Suspende temporariamente a atividade no dispositivo lógico ou habilita novamente a atividade.</span><span class="sxs-lookup"><span data-stu-id="dad07-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="dad07-126">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="dad07-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="dad07-127">Redefine o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="dad07-128">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="dad07-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="dad07-129">Restaura uma configuração anterior e o estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="dad07-130">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="dad07-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="dad07-131">Salva a configuração e o estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="dad07-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dad07-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="dad07-133">Esse método é preterido.</span><span class="sxs-lookup"><span data-stu-id="dad07-133">This method is deprecated.</span></span> <span data-ttu-id="dad07-134">Em vez disso, use a propriedade **SetPowerState** da classe **CIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="dad07-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="dad07-135">**Descrição preterida:** Define o estado de energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="dad07-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dad07-136">Properties</span></span>

<span data-ttu-id="dad07-137">A classe **CIM \_ LogicalDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dad07-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dad07-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="dad07-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-139">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dad07-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dad07-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-141">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ LogicalDevice CIM**.**Disponibilidade**")</span><span class="sxs-lookup"><span data-stu-id="dad07-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-142">Uma matriz que contém informações de disponibilidade sobre o dispositivo lógico, além da propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="dad07-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dad07-143">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="dad07-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dad07-144">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="dad07-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dad07-145">**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="dad07-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dad07-146">**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="dad07-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dad07-147">**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="dad07-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dad07-148">**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="dad07-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dad07-149">**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="dad07-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dad07-150">**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="dad07-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dad07-151">**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="dad07-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dad07-152">**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="dad07-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dad07-153">**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="dad07-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dad07-154">**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="dad07-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dad07-155">Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="dad07-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dad07-156">Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="dad07-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dad07-157">**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="dad07-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dad07-158">**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="dad07-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dad07-159">Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="dad07-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dad07-160">Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="dad07-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dad07-161">**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="dad07-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dad07-162">**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="dad07-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dad07-163">**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="dad07-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dad07-164">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="dad07-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dad07-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-167">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 6,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus "," MIF. \|Dispositivo de host DMTF \| 1,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**AdditionalAvailability**")</span><span class="sxs-lookup"><span data-stu-id="dad07-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-168">Contém a disponibilidade do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dad07-169">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="dad07-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dad07-170">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="dad07-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dad07-171">**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="dad07-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dad07-172">**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="dad07-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dad07-173">**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="dad07-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dad07-174">**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="dad07-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dad07-175">**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="dad07-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dad07-176">**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="dad07-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dad07-177">**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="dad07-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dad07-178">**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="dad07-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dad07-179">**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="dad07-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dad07-180">**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="dad07-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dad07-181">Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="dad07-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dad07-182">Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="dad07-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dad07-183">**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="dad07-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dad07-184">**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="dad07-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dad07-185">Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="dad07-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dad07-186">Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="dad07-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dad07-187">**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="dad07-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dad07-188">**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="dad07-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dad07-189">**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="dad07-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dad07-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dad07-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-193">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dad07-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dad07-194">O nome da classe usada para criar uma instância do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="dad07-195">**CreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="dad07-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dad07-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-199">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dad07-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dad07-200">Um identificador exclusivo do dispositivo lógico, como o endereço.</span><span class="sxs-lookup"><span data-stu-id="dad07-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-201">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="dad07-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-202">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dad07-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-204">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="dad07-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-205">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="dad07-205">This property is deprecated.</span></span> <span data-ttu-id="dad07-206">Em vez disso, use a propriedade **OperationalStatus** da classe **\_ ManagedSystemElement do CIM** .</span><span class="sxs-lookup"><span data-stu-id="dad07-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="dad07-207">**Descrição preterida:** Indica se um erro relatado pela propriedade **LastErrorCode** está limpo.</span><span class="sxs-lookup"><span data-stu-id="dad07-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dad07-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-211">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. ErrorDescription")</span><span class="sxs-lookup"><span data-stu-id="dad07-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-212">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="dad07-212">This property is deprecated.</span></span> <span data-ttu-id="dad07-213">Em vez disso, use a propriedade **ErrorDescription** da classe **CIM \_ DeviceErrorData** .</span><span class="sxs-lookup"><span data-stu-id="dad07-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="dad07-214">**Descrição preterida:** Informações adicionais sobre o erro relatado pela propriedade **LastErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="dad07-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dad07-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-216">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dad07-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-218">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM LogicalDevice**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="dad07-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-219">Uma matriz de cadeias de caracteres que descreve os itens de matriz **OtherIdentifyingInfo** do mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="dad07-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-220">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dad07-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-221">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dad07-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-223">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. LastErrorCode")</span><span class="sxs-lookup"><span data-stu-id="dad07-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-224">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="dad07-224">This property is deprecated.</span></span> <span data-ttu-id="dad07-225">Em vez disso, usamos a propriedade **LastErrorCode** da **classe \_ DeviceErrorData do CIM** .</span><span class="sxs-lookup"><span data-stu-id="dad07-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="dad07-226">**Descrição preterida:** O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-227">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="dad07-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-228">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dad07-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-230">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="dad07-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-231">Essa propriedade foi preterida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="dad07-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="dad07-232">**Descrição preterida:** O tempo máximo em milissegundos, que um dispositivo pode permanecer em um estado temporariamente desabilitado (as propriedades de **disponibilidade** e **AdditionalAvailability** definidas como "21" inativos).</span><span class="sxs-lookup"><span data-stu-id="dad07-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="dad07-233">Um valor de "0" indica que o dispositivo lógico pode permanecer em um estado temporariamente desabilitado indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="dad07-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="dad07-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-235">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dad07-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-237">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="dad07-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-238">Informações que identificam o dispositivo lógico, diferente de **DeviceID**.</span><span class="sxs-lookup"><span data-stu-id="dad07-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-239">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dad07-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-240">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dad07-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dad07-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-242">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities")</span><span class="sxs-lookup"><span data-stu-id="dad07-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-243">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="dad07-243">This property is deprecated.</span></span> <span data-ttu-id="dad07-244">Em vez disso, use a classe **CIM \_ PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="dad07-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="dad07-245">**Descrição preterida:** Uma matriz que contém os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dad07-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dad07-246">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dad07-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dad07-247">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="dad07-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dad07-248">**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="dad07-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dad07-249">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="dad07-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dad07-250">**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="dad07-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dad07-251">**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="dad07-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dad07-252">**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="dad07-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dad07-253">**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="dad07-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dad07-254">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="dad07-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-255">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dad07-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-257">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")</span><span class="sxs-lookup"><span data-stu-id="dad07-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-258">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="dad07-258">This property is deprecated.</span></span> <span data-ttu-id="dad07-259">Em vez disso, use a classe **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="dad07-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="dad07-260">**Descrição preterida: true** se o dispositivo lógico puder ser gerenciado por energia; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="dad07-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-261">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="dad07-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-262">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dad07-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-264">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("horas"), **contador**</span><span class="sxs-lookup"><span data-stu-id="dad07-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="dad07-265">O número de horas consecutivas que o dispositivo lógico foi ligado, desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="dad07-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dad07-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dad07-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-269">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**Enabledstate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Estado operacional da DMTF \| 6,4 ")</span><span class="sxs-lookup"><span data-stu-id="dad07-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-270">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="dad07-270">This property is deprecated.</span></span> <span data-ttu-id="dad07-271">Em vez disso, use a classe **CIM \_ PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="dad07-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="dad07-272">**Descrição preterida:** Indica se o dispositivo lógico está habilitado ou em um estado relacionado.</span><span class="sxs-lookup"><span data-stu-id="dad07-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dad07-273">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="dad07-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dad07-274">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="dad07-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dad07-275">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="dad07-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dad07-276">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="dad07-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dad07-277">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="dad07-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dad07-278">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dad07-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-281">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="dad07-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-282">O nome da classe usada para criar uma instância do sistema que contém o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="dad07-283">**SystemCreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="dad07-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-284">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dad07-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dad07-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-287">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="dad07-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="dad07-288">O nome do sistema que contém o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dad07-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="dad07-289">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="dad07-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad07-290">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dad07-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dad07-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dad07-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad07-292">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("horas"), **contador**</span><span class="sxs-lookup"><span data-stu-id="dad07-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="dad07-293">O número total de horas em que o dispositivo lógico foi ligado.</span><span class="sxs-lookup"><span data-stu-id="dad07-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dad07-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad07-294">Requirements</span></span>



| <span data-ttu-id="dad07-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad07-295">Requirement</span></span> | <span data-ttu-id="dad07-296">Valor</span><span class="sxs-lookup"><span data-stu-id="dad07-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dad07-297">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad07-297">Minimum supported client</span></span><br/> | <span data-ttu-id="dad07-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dad07-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dad07-299">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad07-299">Minimum supported server</span></span><br/> | <span data-ttu-id="dad07-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dad07-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dad07-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="dad07-301">Namespace</span></span><br/>                | <span data-ttu-id="dad07-302">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dad07-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dad07-303">MOF</span><span class="sxs-lookup"><span data-stu-id="dad07-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dad07-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dad07-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dad07-305">DLL</span><span class="sxs-lookup"><span data-stu-id="dad07-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dad07-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dad07-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dad07-307">Confira também</span><span class="sxs-lookup"><span data-stu-id="dad07-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad07-308">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="dad07-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

