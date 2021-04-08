---
description: A \_ classe WMI FloppyController do Win32 representa os recursos e a capacidade de gerenciamento de um controlador de unidade de disquete.
ms.assetid: 8c02847c-8329-4adc-b2a5-149b36aead88
ms.tgt_platform: multiple
title: Classe Win32_FloppyController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyController
- Win32_FloppyController.Reset
- Win32_FloppyController.SetPowerState
- Win32_FloppyController.Availability
- Win32_FloppyController.Caption
- Win32_FloppyController.ConfigManagerErrorCode
- Win32_FloppyController.ConfigManagerUserConfig
- Win32_FloppyController.CreationClassName
- Win32_FloppyController.Description
- Win32_FloppyController.DeviceID
- Win32_FloppyController.ErrorCleared
- Win32_FloppyController.ErrorDescription
- Win32_FloppyController.InstallDate
- Win32_FloppyController.LastErrorCode
- Win32_FloppyController.Manufacturer
- Win32_FloppyController.MaxNumberControlled
- Win32_FloppyController.Name
- Win32_FloppyController.PNPDeviceID
- Win32_FloppyController.PowerManagementCapabilities
- Win32_FloppyController.PowerManagementSupported
- Win32_FloppyController.ProtocolSupported
- Win32_FloppyController.Status
- Win32_FloppyController.StatusInfo
- Win32_FloppyController.SystemCreationClassName
- Win32_FloppyController.SystemName
- Win32_FloppyController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7aac44fb8e2b0a91ca3794f234a31cd4c25a4b5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920492"
---
# <a name="win32_floppycontroller-class"></a><span data-ttu-id="d86fc-103">\_Classe Win32 FloppyController</span><span class="sxs-lookup"><span data-stu-id="d86fc-103">Win32\_FloppyController class</span></span>

<span data-ttu-id="d86fc-104">\[**Win32 \_ O FloppyController** não está mais disponível para uso a partir do Windows 10 e do Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="d86fc-104">\[**Win32\_FloppyController** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="d86fc-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ FloppyController do Win32** representa os recursos e a capacidade de gerenciamento de um controlador de unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="d86fc-105">The **Win32\_FloppyController** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a floppy disk drive controller.</span></span>

<span data-ttu-id="d86fc-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d86fc-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d86fc-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d86fc-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86fc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d86fc-108">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{2A7DC003-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="d86fc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d86fc-109">Members</span></span>

<span data-ttu-id="d86fc-110">A classe **Win32 \_ FloppyController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d86fc-110">The **Win32\_FloppyController** class has these types of members:</span></span>

-   [<span data-ttu-id="d86fc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d86fc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d86fc-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d86fc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d86fc-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d86fc-113">Methods</span></span>

<span data-ttu-id="d86fc-114">A classe **Win32 \_ FloppyController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d86fc-114">The **Win32\_FloppyController** class has these methods.</span></span>



| <span data-ttu-id="d86fc-115">Método</span><span class="sxs-lookup"><span data-stu-id="d86fc-115">Method</span></span>            | <span data-ttu-id="d86fc-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d86fc-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86fc-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d86fc-117">**Reset**</span></span>         | <span data-ttu-id="d86fc-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-118">Not implemented.</span></span> <span data-ttu-id="d86fc-119">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ controlador CIM**](cim-controller.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="d86fc-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d86fc-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d86fc-120">**SetPowerState**</span></span> | <span data-ttu-id="d86fc-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-121">Not implemented.</span></span> <span data-ttu-id="d86fc-122">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ controlador CIM**](cim-controller.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="d86fc-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d86fc-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d86fc-123">Properties</span></span>

<span data-ttu-id="d86fc-124">A classe **Win32 \_ FloppyController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d86fc-124">The **Win32\_FloppyController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d86fc-125">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d86fc-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d86fc-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d86fc-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-129">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-129">Availability and status of the device.</span></span>

<span data-ttu-id="d86fc-130">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d86fc-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d86fc-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d86fc-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="d86fc-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d86fc-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d86fc-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-134">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="d86fc-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d86fc-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="d86fc-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d86fc-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="d86fc-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d86fc-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="d86fc-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d86fc-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="d86fc-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d86fc-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="d86fc-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d86fc-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="d86fc-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d86fc-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d86fc-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d86fc-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d86fc-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d86fc-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="d86fc-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d86fc-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="d86fc-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-145">Economia de energia-desconhecido</span><span class="sxs-lookup"><span data-stu-id="d86fc-145">Power Save - Unknown</span></span>

<span data-ttu-id="d86fc-146">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d86fc-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d86fc-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="d86fc-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-148">Economia de energia-modo de baixa energia</span><span class="sxs-lookup"><span data-stu-id="d86fc-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="d86fc-149">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d86fc-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d86fc-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-151">Economia de energia-em espera</span><span class="sxs-lookup"><span data-stu-id="d86fc-151">Power Save - Standby</span></span>

<span data-ttu-id="d86fc-152">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d86fc-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="d86fc-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d86fc-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="d86fc-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-155">Economia de energia-aviso</span><span class="sxs-lookup"><span data-stu-id="d86fc-155">Power Save - Warning</span></span>

<span data-ttu-id="d86fc-156">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="d86fc-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d86fc-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d86fc-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-158">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="d86fc-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d86fc-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="d86fc-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-160">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="d86fc-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d86fc-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d86fc-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-162">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d86fc-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="d86fc-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-164">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="d86fc-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d86fc-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d86fc-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-168">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d86fc-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-169">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="d86fc-169">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d86fc-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d86fc-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d86fc-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-174">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d86fc-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-175">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d86fc-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d86fc-176">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d86fc-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d86fc-178"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="d86fc-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-179">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d86fc-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d86fc-181">(1)</span><span class="sxs-lookup"><span data-stu-id="d86fc-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-182">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d86fc-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d86fc-184">(2)</span><span class="sxs-lookup"><span data-stu-id="d86fc-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d86fc-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d86fc-186">(3)</span><span class="sxs-lookup"><span data-stu-id="d86fc-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-187">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="d86fc-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d86fc-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d86fc-189">(4)</span><span class="sxs-lookup"><span data-stu-id="d86fc-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-190">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-190">Device is not working properly.</span></span> <span data-ttu-id="d86fc-191">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="d86fc-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d86fc-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d86fc-193">(5)</span><span class="sxs-lookup"><span data-stu-id="d86fc-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-194">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="d86fc-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d86fc-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d86fc-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="d86fc-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-197">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d86fc-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d86fc-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d86fc-199">(7)</span><span class="sxs-lookup"><span data-stu-id="d86fc-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d86fc-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d86fc-201">(8)</span><span class="sxs-lookup"><span data-stu-id="d86fc-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-202">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d86fc-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d86fc-204">(9)</span><span class="sxs-lookup"><span data-stu-id="d86fc-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-205">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-205">Device is not working properly.</span></span> <span data-ttu-id="d86fc-206">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d86fc-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d86fc-208">(10)</span><span class="sxs-lookup"><span data-stu-id="d86fc-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-209">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d86fc-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d86fc-211">(11)</span><span class="sxs-lookup"><span data-stu-id="d86fc-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-212">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d86fc-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d86fc-214">12</span><span class="sxs-lookup"><span data-stu-id="d86fc-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-215">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="d86fc-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d86fc-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d86fc-217">(13)</span><span class="sxs-lookup"><span data-stu-id="d86fc-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-218">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d86fc-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d86fc-220">(14)</span><span class="sxs-lookup"><span data-stu-id="d86fc-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-221">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d86fc-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d86fc-223">(15)</span><span class="sxs-lookup"><span data-stu-id="d86fc-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-224">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="d86fc-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d86fc-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d86fc-226">(16)</span><span class="sxs-lookup"><span data-stu-id="d86fc-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-227">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="d86fc-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d86fc-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d86fc-229">(17)</span><span class="sxs-lookup"><span data-stu-id="d86fc-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-230">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d86fc-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d86fc-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d86fc-232">(18)</span><span class="sxs-lookup"><span data-stu-id="d86fc-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-233">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="d86fc-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d86fc-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d86fc-235">(19)</span><span class="sxs-lookup"><span data-stu-id="d86fc-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d86fc-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d86fc-237">(20)</span><span class="sxs-lookup"><span data-stu-id="d86fc-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-238">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="d86fc-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d86fc-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d86fc-240">(21)</span><span class="sxs-lookup"><span data-stu-id="d86fc-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-241">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="d86fc-241">System failure.</span></span> <span data-ttu-id="d86fc-242">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="d86fc-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d86fc-243">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d86fc-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d86fc-245">(22)</span><span class="sxs-lookup"><span data-stu-id="d86fc-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-246">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d86fc-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d86fc-248">(23)</span><span class="sxs-lookup"><span data-stu-id="d86fc-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-249">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="d86fc-249">System failure.</span></span> <span data-ttu-id="d86fc-250">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="d86fc-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d86fc-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d86fc-252">(24)</span><span class="sxs-lookup"><span data-stu-id="d86fc-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-253">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="d86fc-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d86fc-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d86fc-255">(25)</span><span class="sxs-lookup"><span data-stu-id="d86fc-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-256">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d86fc-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d86fc-258">(26)</span><span class="sxs-lookup"><span data-stu-id="d86fc-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d86fc-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d86fc-261">(27)</span><span class="sxs-lookup"><span data-stu-id="d86fc-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-262">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="d86fc-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d86fc-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d86fc-264">(28)</span><span class="sxs-lookup"><span data-stu-id="d86fc-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-265">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="d86fc-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d86fc-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d86fc-267">(29)</span><span class="sxs-lookup"><span data-stu-id="d86fc-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-268">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-268">Device is disabled.</span></span> <span data-ttu-id="d86fc-269">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="d86fc-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d86fc-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d86fc-271">(30)</span><span class="sxs-lookup"><span data-stu-id="d86fc-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-272">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d86fc-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d86fc-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d86fc-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d86fc-274">(31)</span><span class="sxs-lookup"><span data-stu-id="d86fc-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-275">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-275">Device is not working properly.</span></span> <span data-ttu-id="d86fc-276">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="d86fc-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d86fc-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d86fc-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-278">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d86fc-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-280">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d86fc-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-281">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d86fc-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d86fc-282">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d86fc-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-286">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d86fc-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-287">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="d86fc-287">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d86fc-288">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="d86fc-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d86fc-289">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-290">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d86fc-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-293">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="d86fc-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-294">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d86fc-294">Description of the object.</span></span>

<span data-ttu-id="d86fc-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d86fc-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-299">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d86fc-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-300">Identificador exclusivo do controlador de disquete.</span><span class="sxs-lookup"><span data-stu-id="d86fc-300">Unique identifier of the floppy controller.</span></span>

<span data-ttu-id="d86fc-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d86fc-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-303">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d86fc-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-305">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-305">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d86fc-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d86fc-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-310">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d86fc-310">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="d86fc-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-312">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d86fc-312">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-313">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d86fc-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-315">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="d86fc-315">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-316">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-316">Date and time the object is installed.</span></span> <span data-ttu-id="d86fc-317">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-317">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d86fc-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-319">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d86fc-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-320">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d86fc-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-322">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d86fc-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d86fc-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-324">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="d86fc-324">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-327">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="d86fc-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-328">Nome do fabricante do controlador de disquete.</span><span class="sxs-lookup"><span data-stu-id="d86fc-328">Name of the floppy controller manufacturer.</span></span>

<span data-ttu-id="d86fc-329">Exemplo: "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="d86fc-329">Example: "Microsoft"</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-330">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="d86fc-330">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d86fc-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="d86fc-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-334">Número máximo de entidades diretamente endereçáveis às quais este controlador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="d86fc-334">Maximum number of directly addressable entities that this controller supports.</span></span> <span data-ttu-id="d86fc-335">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d86fc-335">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="d86fc-336">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-336">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-337">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d86fc-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-340">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d86fc-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-341">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="d86fc-341">Label for the object.</span></span> <span data-ttu-id="d86fc-342">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="d86fc-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d86fc-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d86fc-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-347">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d86fc-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-348">Identificador de dispositivo do Windows Plug and Play para o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d86fc-348">Windows Plug and Play device identifier for the logical device.</span></span>

<span data-ttu-id="d86fc-349">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d86fc-349">Example: "\*PNP030b"</span></span>

<span data-ttu-id="d86fc-350">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d86fc-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-352">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d86fc-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-354">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d86fc-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d86fc-355">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d86fc-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d86fc-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d86fc-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="d86fc-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d86fc-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d86fc-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d86fc-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d86fc-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-360">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d86fc-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d86fc-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d86fc-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-362">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="d86fc-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d86fc-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="d86fc-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-364">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d86fc-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d86fc-365">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d86fc-366">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d86fc-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d86fc-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="d86fc-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-368">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="d86fc-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d86fc-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="d86fc-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d86fc-370">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="d86fc-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d86fc-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d86fc-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-372">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d86fc-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-374">Se **for true**, o dispositivo poderá ser gerenciado por energia, o que significa que ele pode ser colocado no modo de suspensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d86fc-374">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="d86fc-375">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="d86fc-375">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d86fc-376">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-376">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-377">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="d86fc-377">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-378">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d86fc-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-380">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="d86fc-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-381">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="d86fc-381">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="d86fc-382">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-382">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="d86fc-383">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="d86fc-383">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d86fc-384">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d86fc-384">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d86fc-385">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="d86fc-385">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="d86fc-386">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="d86fc-386">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="d86fc-387">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="d86fc-387">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="d86fc-388">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="d86fc-388">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="d86fc-389">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="d86fc-389">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="d86fc-390">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="d86fc-390">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="d86fc-391">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="d86fc-391">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="d86fc-392">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="d86fc-392">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="d86fc-393">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="d86fc-393">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="d86fc-394">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="d86fc-394">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="d86fc-395">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="d86fc-395">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="d86fc-396">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="d86fc-396">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="d86fc-397">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="d86fc-397">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="d86fc-398">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="d86fc-398">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="d86fc-399">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="d86fc-399">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="d86fc-400">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="d86fc-400">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="d86fc-401">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="d86fc-401">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d86fc-402">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="d86fc-402">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="d86fc-403">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="d86fc-403">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="d86fc-404">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="d86fc-404">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="d86fc-405">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="d86fc-405">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="d86fc-406">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="d86fc-406">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="d86fc-407">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="d86fc-407">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="d86fc-408">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="d86fc-408">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="d86fc-409">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="d86fc-409">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="d86fc-410">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="d86fc-410">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="d86fc-411">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="d86fc-411">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="d86fc-412">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="d86fc-412">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="d86fc-413">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="d86fc-413">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="d86fc-414">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="d86fc-414">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="d86fc-415">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="d86fc-415">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="d86fc-416">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="d86fc-416">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="d86fc-417">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="d86fc-417">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="d86fc-418">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="d86fc-418">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="d86fc-419">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="d86fc-419">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="d86fc-420">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="d86fc-420">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="d86fc-421">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="d86fc-421">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="d86fc-422">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="d86fc-422">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="d86fc-423">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="d86fc-423">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="d86fc-424">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="d86fc-424">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="d86fc-425">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="d86fc-425">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="d86fc-426">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="d86fc-426">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="d86fc-427">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="d86fc-427">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="d86fc-428">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="d86fc-428">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="d86fc-429">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="d86fc-429">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="d86fc-430">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="d86fc-430">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d86fc-431">**Status**</span><span class="sxs-lookup"><span data-stu-id="d86fc-431">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-432">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-434">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d86fc-434">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-435">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d86fc-435">Current status of the object.</span></span> <span data-ttu-id="d86fc-436">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d86fc-436">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d86fc-437">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d86fc-437">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d86fc-438">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="d86fc-438">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d86fc-439">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-439">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d86fc-440">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="d86fc-440">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d86fc-441">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d86fc-442">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="d86fc-442">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d86fc-443">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d86fc-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d86fc-444">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="d86fc-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d86fc-445">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d86fc-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d86fc-446">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="d86fc-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d86fc-447">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d86fc-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d86fc-448">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d86fc-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d86fc-449">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="d86fc-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d86fc-450">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="d86fc-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d86fc-451">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="d86fc-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d86fc-452">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d86fc-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d86fc-453">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="d86fc-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d86fc-454">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="d86fc-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d86fc-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d86fc-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-456">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d86fc-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-458">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="d86fc-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-459">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d86fc-459">State of the logical device.</span></span> <span data-ttu-id="d86fc-460">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-460">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d86fc-461">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d86fc-462">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d86fc-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d86fc-463">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="d86fc-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d86fc-464">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d86fc-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d86fc-465">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d86fc-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d86fc-466">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="d86fc-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d86fc-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d86fc-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-468">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-470">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d86fc-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-471">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-471">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d86fc-472">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d86fc-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d86fc-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-476">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d86fc-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-477">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d86fc-477">Name of the scoping system.</span></span>

<span data-ttu-id="d86fc-478">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d86fc-479">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="d86fc-479">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d86fc-480">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d86fc-480">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d86fc-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d86fc-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d86fc-482">Data e hora da última redefinição do controlador.</span><span class="sxs-lookup"><span data-stu-id="d86fc-482">Date and time the controller was last reset.</span></span> <span data-ttu-id="d86fc-483">Isso pode significar que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="d86fc-483">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="d86fc-484">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-484">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d86fc-485">Comentários</span><span class="sxs-lookup"><span data-stu-id="d86fc-485">Remarks</span></span>

<span data-ttu-id="d86fc-486">A classe **Win32 \_ FloppyController** é derivada do [**\_ controlador CIM**](cim-controller.md) derivado de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d86fc-486">The **Win32\_FloppyController** class is derived from [**CIM\_Controller**](cim-controller.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d86fc-487">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d86fc-487">Requirements</span></span>



| <span data-ttu-id="d86fc-488">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86fc-488">Requirement</span></span> | <span data-ttu-id="d86fc-489">Valor</span><span class="sxs-lookup"><span data-stu-id="d86fc-489">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d86fc-490">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d86fc-490">Minimum supported client</span></span><br/> | <span data-ttu-id="d86fc-491">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d86fc-491">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d86fc-492">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d86fc-492">Minimum supported server</span></span><br/> | <span data-ttu-id="d86fc-493">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d86fc-493">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d86fc-494">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d86fc-494">End of client support</span></span><br/>    | <span data-ttu-id="d86fc-495">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d86fc-495">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="d86fc-496">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d86fc-496">End of server support</span></span><br/>    | <span data-ttu-id="d86fc-497">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d86fc-497">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="d86fc-498">Namespace</span><span class="sxs-lookup"><span data-stu-id="d86fc-498">Namespace</span></span><br/>                | <span data-ttu-id="d86fc-499">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d86fc-499">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d86fc-500">MOF</span><span class="sxs-lookup"><span data-stu-id="d86fc-500">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d86fc-501"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d86fc-501"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d86fc-502">DLL</span><span class="sxs-lookup"><span data-stu-id="d86fc-502">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d86fc-503"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d86fc-503"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86fc-504">Confira também</span><span class="sxs-lookup"><span data-stu-id="d86fc-504">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86fc-505">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="d86fc-505">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="d86fc-506">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d86fc-506">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

