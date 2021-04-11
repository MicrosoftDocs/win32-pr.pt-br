---
description: O Win32 \_ PCMCIAController &\# 32; A classe WMI gerencia os recursos de um dispositivo de controlador de placa de memória de computador pessoal (PCMCIA de um adaptador de PC).
ms.assetid: 541f8ebd-e976-425a-817a-72ab151e8b93
ms.tgt_platform: multiple
title: Classe Win32_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PCMCIAController
- Win32_PCMCIAController.Reset
- Win32_PCMCIAController.SetPowerState
- Win32_PCMCIAController.Availability
- Win32_PCMCIAController.Caption
- Win32_PCMCIAController.ConfigManagerErrorCode
- Win32_PCMCIAController.ConfigManagerUserConfig
- Win32_PCMCIAController.CreationClassName
- Win32_PCMCIAController.Description
- Win32_PCMCIAController.DeviceID
- Win32_PCMCIAController.ErrorCleared
- Win32_PCMCIAController.ErrorDescription
- Win32_PCMCIAController.InstallDate
- Win32_PCMCIAController.LastErrorCode
- Win32_PCMCIAController.Manufacturer
- Win32_PCMCIAController.MaxNumberControlled
- Win32_PCMCIAController.Name
- Win32_PCMCIAController.PNPDeviceID
- Win32_PCMCIAController.PowerManagementCapabilities
- Win32_PCMCIAController.PowerManagementSupported
- Win32_PCMCIAController.ProtocolSupported
- Win32_PCMCIAController.Status
- Win32_PCMCIAController.StatusInfo
- Win32_PCMCIAController.SystemCreationClassName
- Win32_PCMCIAController.SystemName
- Win32_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 463be0c3924130ce0e2c0ff84c3852398b6cff99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164145"
---
# <a name="win32_pcmciacontroller-class"></a><span data-ttu-id="5a2e2-103">\_Classe Win32 PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="5a2e2-103">Win32\_PCMCIAController class</span></span>

<span data-ttu-id="5a2e2-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PCMCIAController do Win32** gerencia os recursos de um dispositivo de controlador de placa de memória de computador pessoal (PCMCIA de um PC Card).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-104">The **Win32\_PCMCIAController** [WMI class](../wmisdk/retrieving-a-class.md) manages the capabilities of a Personal Computer Memory Card Interface Adapter (PCMCIA of a PC Card) controller device.</span></span>

<span data-ttu-id="5a2e2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5a2e2-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a2e2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{98C7E2C6-D592-11d2-B355-00105A0A323A}"), AMENDMENT]
class Win32_PCMCIAController : CIM_PCMCIAController
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

## <a name="members"></a><span data-ttu-id="5a2e2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5a2e2-108">Members</span></span>

<span data-ttu-id="5a2e2-109">A classe **Win32 \_ PCMCIAController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5a2e2-109">The **Win32\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="5a2e2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a2e2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a2e2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a2e2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a2e2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a2e2-112">Methods</span></span>

<span data-ttu-id="5a2e2-113">A classe **Win32 \_ PCMCIAController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-113">The **Win32\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="5a2e2-114">Método</span><span class="sxs-lookup"><span data-stu-id="5a2e2-114">Method</span></span>            | <span data-ttu-id="5a2e2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a2e2-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2e2-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-116">**Reset**</span></span>         | <span data-ttu-id="5a2e2-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-117">Not implemented.</span></span> <span data-ttu-id="5a2e2-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span><br/>                 |
| <span data-ttu-id="5a2e2-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-119">**SetPowerState**</span></span> | <span data-ttu-id="5a2e2-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-120">Not implemented.</span></span> <span data-ttu-id="5a2e2-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5a2e2-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a2e2-122">Properties</span></span>

<span data-ttu-id="5a2e2-123">A classe **Win32 \_ PCMCIAController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-123">The **Win32\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a2e2-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-128">Availability and status of the device.</span></span>

<span data-ttu-id="5a2e2-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a2e2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a2e2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5a2e2-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="5a2e2-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5a2e2-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5a2e2-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5a2e2-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5a2e2-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="5a2e2-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5a2e2-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5a2e2-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5a2e2-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5a2e2-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5a2e2-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5a2e2-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5a2e2-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5a2e2-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5a2e2-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5a2e2-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5a2e2-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-153">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-153">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5a2e2-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-155">Não está pronto.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-155">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5a2e2-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-157">Não configurado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-157">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5a2e2-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-159">Ativa.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-159">Quiesced.</span></span>

<span data-ttu-id="5a2e2-160">O controlador PCMCIA não está disponível.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-160">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a2e2-161">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-164">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-165">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-165">Short description of the object.</span></span>

<span data-ttu-id="5a2e2-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-170">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-171">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5a2e2-172">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5a2e2-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5a2e2-174"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-175">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5a2e2-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5a2e2-177">(1)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-178">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5a2e2-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5a2e2-180">(2)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5a2e2-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5a2e2-182">(3)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-183">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5a2e2-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5a2e2-185">(4)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-186">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-186">Device is not working properly.</span></span> <span data-ttu-id="5a2e2-187">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5a2e2-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5a2e2-189">(5)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-190">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5a2e2-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5a2e2-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-193">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5a2e2-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5a2e2-195">(7)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5a2e2-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5a2e2-197">(8)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-198">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5a2e2-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5a2e2-200">(9)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-201">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-201">Device is not working properly.</span></span> <span data-ttu-id="5a2e2-202">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5a2e2-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5a2e2-204">(10)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-205">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5a2e2-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5a2e2-207">(11)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-208">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5a2e2-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5a2e2-210">12</span><span class="sxs-lookup"><span data-stu-id="5a2e2-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-211">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5a2e2-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5a2e2-213">(13)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-214">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5a2e2-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5a2e2-216">(14)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-217">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5a2e2-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5a2e2-219">(15)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-220">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5a2e2-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5a2e2-222">(16)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-223">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5a2e2-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5a2e2-225">(17)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-226">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5a2e2-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5a2e2-228">(18)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-229">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5a2e2-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5a2e2-231">(19)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5a2e2-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5a2e2-233">(20)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-234">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5a2e2-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5a2e2-236">(21)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-237">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-237">System failure.</span></span> <span data-ttu-id="5a2e2-238">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5a2e2-239">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5a2e2-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5a2e2-241">(22)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-242">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5a2e2-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5a2e2-244">(23)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-245">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-245">System failure.</span></span> <span data-ttu-id="5a2e2-246">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5a2e2-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5a2e2-248">(24)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-249">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5a2e2-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5a2e2-251">(25)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-252">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5a2e2-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5a2e2-254">(26)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-255">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5a2e2-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5a2e2-257">(27)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-258">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5a2e2-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5a2e2-260">(28)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-261">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5a2e2-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5a2e2-263">(29)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-264">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-264">Device is disabled.</span></span> <span data-ttu-id="5a2e2-265">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5a2e2-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5a2e2-267">(30)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-268">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5a2e2-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5a2e2-270">(31)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-271">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-271">Device is not working properly.</span></span> <span data-ttu-id="5a2e2-272">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a2e2-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-274">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-276">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-277">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5a2e2-278">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-282">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-283">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5a2e2-284">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5a2e2-285">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-286">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-289">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-290">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-290">Description of the object.</span></span>

<span data-ttu-id="5a2e2-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-295">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-295">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-296">Identificador exclusivo deste dispositivo com outros periféricos usando o Plug and Play BIOS.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-296">Unique identifier of this device with other peripherals using the Plug and Play BIOS.</span></span> <span data-ttu-id="5a2e2-297">Essa propriedade é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-297">This property is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-298">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-298">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-299">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-299">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-301">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-301">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="5a2e2-302">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-303">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-303">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-306">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-306">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="5a2e2-307">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-309">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-311">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-312">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-312">Date and time the object was installed.</span></span> <span data-ttu-id="5a2e2-313">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5a2e2-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-315">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-315">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-316">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-318">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-318">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5a2e2-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-320">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-320">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-323">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-323">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-324">Nome do fabricante do controlador PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-324">Name of the PCMCIA controller manufacturer.</span></span>

<span data-ttu-id="5a2e2-325">Essa propriedade é herdada do [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-325">This property is inherited from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span>

<span data-ttu-id="5a2e2-326">Exemplo: "Acme"</span><span class="sxs-lookup"><span data-stu-id="5a2e2-326">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-327">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-327">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-328">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-330">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-331">Número máximo de entidades diretamente endereçáveis com suporte por este controlador.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-331">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="5a2e2-332">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-332">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="5a2e2-333">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-333">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-334">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-337">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-338">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-338">Label by which the object is known.</span></span> <span data-ttu-id="5a2e2-339">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5a2e2-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-341">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-341">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-344">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-344">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-345">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-345">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5a2e2-346">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5a2e2-347">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5a2e2-347">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-348">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-348">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-349">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-349">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-351">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-351">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5a2e2-352">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-352">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a2e2-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5a2e2-354"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-354"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a2e2-355"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-355"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a2e2-356"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-356"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-357">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-357">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5a2e2-358"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-358"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-359">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-359">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5a2e2-360"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-360"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-361">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5a2e2-361">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5a2e2-362">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-362">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5a2e2-363">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-363">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5a2e2-364"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-364"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-365">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5a2e2-366"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-366"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5a2e2-367">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="5a2e2-367">Timed Power-On Supported</span></span>

<span data-ttu-id="5a2e2-368">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a2e2-369">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-369">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-370">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-372">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-372">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="5a2e2-373">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-373">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="5a2e2-374">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-375">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-375">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-378">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-379">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="5a2e2-379">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="5a2e2-380">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-380">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="5a2e2-381">Os valores são mostrados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-381">The values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a2e2-382">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-382">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a2e2-383">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-383">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="5a2e2-384">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-384">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="5a2e2-385">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-385">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="5a2e2-386">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-386">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="5a2e2-387">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-387">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="5a2e2-388">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-388">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="5a2e2-389">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-389">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="5a2e2-390">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-390">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="5a2e2-391">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-391">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="5a2e2-392">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-392">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="5a2e2-393">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-393">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="5a2e2-394">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-394">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="5a2e2-395">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-395">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="5a2e2-396">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-396">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="5a2e2-397">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-397">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="5a2e2-398">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-398">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="5a2e2-399">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-399">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="5a2e2-400">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-400">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="5a2e2-401">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-401">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="5a2e2-402">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-402">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="5a2e2-403">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-403">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="5a2e2-404">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-404">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="5a2e2-405">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-405">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="5a2e2-406">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-406">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="5a2e2-407">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-407">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="5a2e2-408">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-408">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="5a2e2-409">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-409">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="5a2e2-410">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-410">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="5a2e2-411">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-411">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="5a2e2-412">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-412">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="5a2e2-413">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-413">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="5a2e2-414">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-414">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="5a2e2-415">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-415">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="5a2e2-416">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-416">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="5a2e2-417">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-417">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="5a2e2-418">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-418">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="5a2e2-419">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-419">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="5a2e2-420">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-420">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="5a2e2-421">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-421">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="5a2e2-422">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-422">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="5a2e2-423">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-423">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="5a2e2-424">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-424">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="5a2e2-425">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-425">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="5a2e2-426">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-426">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="5a2e2-427">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-427">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="5a2e2-428">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-428">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a2e2-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-432">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-433">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-433">Current status of the object.</span></span> <span data-ttu-id="5a2e2-434">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5a2e2-435">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5a2e2-436">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5a2e2-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5a2e2-437">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5a2e2-438">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5a2e2-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5a2e2-440">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5a2e2-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5a2e2-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5a2e2-442">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5a2e2-443">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a2e2-444">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5a2e2-445">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5a2e2-446">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5a2e2-447">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5a2e2-448">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5a2e2-449">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5a2e2-450">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5a2e2-451">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5a2e2-452">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a2e2-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-456">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="5a2e2-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-457">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-457">State of the logical device.</span></span> <span data-ttu-id="5a2e2-458">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5a2e2-459">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a2e2-460">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a2e2-461">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a2e2-462">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a2e2-463">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5a2e2-464">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a2e2-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-468">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-469">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="5a2e2-470">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-474">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5a2e2-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-475">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-475">Name of the scoping system.</span></span>

<span data-ttu-id="5a2e2-476">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a2e2-477">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-477">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a2e2-478">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-478">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a2e2-479">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a2e2-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a2e2-480">Data e hora da última redefinição do controlador.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-480">Date and time the controller was last reset.</span></span> <span data-ttu-id="5a2e2-481">Isso pode significar que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="5a2e2-481">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="5a2e2-482">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-482">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a2e2-483">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a2e2-483">Remarks</span></span>

<span data-ttu-id="5a2e2-484">A classe **Win32 \_ PCMCIAController** é derivada de [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5a2e2-484">The **Win32\_PCMCIAController** class is derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2e2-485">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a2e2-485">Requirements</span></span>



| <span data-ttu-id="5a2e2-486">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a2e2-486">Requirement</span></span> | <span data-ttu-id="5a2e2-487">Valor</span><span class="sxs-lookup"><span data-stu-id="5a2e2-487">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2e2-488">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a2e2-488">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2e2-489">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a2e2-489">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a2e2-490">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a2e2-490">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2e2-491">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a2e2-491">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a2e2-492">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a2e2-492">Namespace</span></span><br/>                | <span data-ttu-id="5a2e2-493">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5a2e2-493">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5a2e2-494">MOF</span><span class="sxs-lookup"><span data-stu-id="5a2e2-494">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a2e2-495"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a2e2-495"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a2e2-496">DLL</span><span class="sxs-lookup"><span data-stu-id="5a2e2-496">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a2e2-497"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a2e2-497"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2e2-498">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a2e2-498">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2e2-499">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="5a2e2-499">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="5a2e2-500">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="5a2e2-500">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
