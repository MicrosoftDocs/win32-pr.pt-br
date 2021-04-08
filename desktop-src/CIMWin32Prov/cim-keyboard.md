---
description: A \_ classe de teclado CIM representa os recursos e o gerenciamento do dispositivo lógico do teclado.
ms.assetid: c465a731-03dd-4418-8b16-96dc2c8b60b5
ms.tgt_platform: multiple
title: Classe CIM_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Keyboard
- CIM_Keyboard.Availability
- CIM_Keyboard.Caption
- CIM_Keyboard.ConfigManagerErrorCode
- CIM_Keyboard.ConfigManagerUserConfig
- CIM_Keyboard.CreationClassName
- CIM_Keyboard.Description
- CIM_Keyboard.DeviceID
- CIM_Keyboard.ErrorCleared
- CIM_Keyboard.ErrorDescription
- CIM_Keyboard.InstallDate
- CIM_Keyboard.IsLocked
- CIM_Keyboard.LastErrorCode
- CIM_Keyboard.Layout
- CIM_Keyboard.Name
- CIM_Keyboard.NumberOfFunctionKeys
- CIM_Keyboard.Password
- CIM_Keyboard.PNPDeviceID
- CIM_Keyboard.PowerManagementCapabilities
- CIM_Keyboard.PowerManagementSupported
- CIM_Keyboard.Status
- CIM_Keyboard.StatusInfo
- CIM_Keyboard.SystemCreationClassName
- CIM_Keyboard.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7424601632a9d6a0bedcbcde7ab3c27cf27c69cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089272"
---
# <a name="cim_keyboard-class"></a><span data-ttu-id="982cc-103">\_Classe de teclado CIM</span><span class="sxs-lookup"><span data-stu-id="982cc-103">CIM\_Keyboard class</span></span>

<span data-ttu-id="982cc-104">A classe de **\_ teclado CIM** representa os recursos e o gerenciamento do dispositivo lógico do teclado.</span><span class="sxs-lookup"><span data-stu-id="982cc-104">The **CIM\_Keyboard** class represents the capabilities and management of the keyboard logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="982cc-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="982cc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="982cc-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="982cc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="982cc-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="982cc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="982cc-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="982cc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="982cc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="982cc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C534-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Keyboard : CIM_UserDevice
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
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Layout;
  string   Name;
  uint16   NumberOfFunctionKeys;
  uint16   Password;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="982cc-110">Membros</span><span class="sxs-lookup"><span data-stu-id="982cc-110">Members</span></span>

<span data-ttu-id="982cc-111">A classe de **\_ teclado CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="982cc-111">The **CIM\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="982cc-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="982cc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="982cc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="982cc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="982cc-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="982cc-114">Methods</span></span>

<span data-ttu-id="982cc-115">A classe de **\_ teclado CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="982cc-115">The **CIM\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="982cc-116">Método</span><span class="sxs-lookup"><span data-stu-id="982cc-116">Method</span></span>                                                              | <span data-ttu-id="982cc-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="982cc-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="982cc-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="982cc-118">**Reset**</span></span>](reset-method-in-class-cim-keyboard.md)                 | <span data-ttu-id="982cc-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="982cc-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="982cc-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="982cc-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="982cc-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="982cc-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-keyboard.md) | <span data-ttu-id="982cc-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="982cc-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="982cc-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="982cc-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="982cc-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="982cc-124">Properties</span></span>

<span data-ttu-id="982cc-125">A classe de **\_ teclado CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="982cc-125">The **CIM\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="982cc-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="982cc-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982cc-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="982cc-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-130">Availability and status of the device.</span></span>

<span data-ttu-id="982cc-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="982cc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="982cc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="982cc-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="982cc-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="982cc-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="982cc-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="982cc-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="982cc-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="982cc-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="982cc-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="982cc-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="982cc-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="982cc-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="982cc-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="982cc-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="982cc-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="982cc-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="982cc-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="982cc-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="982cc-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="982cc-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="982cc-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="982cc-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="982cc-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="982cc-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="982cc-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="982cc-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="982cc-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="982cc-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="982cc-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="982cc-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="982cc-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="982cc-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="982cc-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="982cc-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="982cc-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="982cc-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="982cc-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="982cc-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="982cc-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="982cc-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="982cc-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="982cc-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="982cc-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="982cc-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="982cc-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="982cc-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="982cc-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="982cc-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="982cc-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="982cc-161">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="982cc-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-164">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="982cc-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-165">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="982cc-165">Short textual description of the object.</span></span>

<span data-ttu-id="982cc-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="982cc-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="982cc-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-170">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="982cc-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-171">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="982cc-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="982cc-172">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="982cc-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="982cc-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="982cc-174"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="982cc-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-175">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="982cc-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="982cc-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="982cc-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="982cc-177">(1)</span><span class="sxs-lookup"><span data-stu-id="982cc-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-178">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="982cc-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="982cc-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="982cc-180">(2)</span><span class="sxs-lookup"><span data-stu-id="982cc-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="982cc-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="982cc-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="982cc-182">(3)</span><span class="sxs-lookup"><span data-stu-id="982cc-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-183">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="982cc-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="982cc-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="982cc-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="982cc-185">(4)</span><span class="sxs-lookup"><span data-stu-id="982cc-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-186">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="982cc-186">Device is not working properly.</span></span> <span data-ttu-id="982cc-187">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="982cc-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="982cc-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="982cc-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="982cc-189">(5)</span><span class="sxs-lookup"><span data-stu-id="982cc-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-190">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="982cc-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="982cc-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="982cc-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="982cc-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="982cc-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-193">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="982cc-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="982cc-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="982cc-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="982cc-195">(7)</span><span class="sxs-lookup"><span data-stu-id="982cc-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="982cc-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="982cc-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="982cc-197">(8)</span><span class="sxs-lookup"><span data-stu-id="982cc-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-198">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="982cc-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="982cc-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="982cc-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="982cc-200">(9)</span><span class="sxs-lookup"><span data-stu-id="982cc-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-201">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="982cc-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="982cc-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="982cc-203">(10)</span><span class="sxs-lookup"><span data-stu-id="982cc-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-204">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="982cc-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="982cc-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="982cc-206">(11)</span><span class="sxs-lookup"><span data-stu-id="982cc-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-207">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="982cc-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="982cc-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="982cc-209">12</span><span class="sxs-lookup"><span data-stu-id="982cc-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-210">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="982cc-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="982cc-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="982cc-212">(13)</span><span class="sxs-lookup"><span data-stu-id="982cc-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-213">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="982cc-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="982cc-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="982cc-215">(14)</span><span class="sxs-lookup"><span data-stu-id="982cc-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-216">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="982cc-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="982cc-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="982cc-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="982cc-218">(15)</span><span class="sxs-lookup"><span data-stu-id="982cc-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-219">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="982cc-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="982cc-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="982cc-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="982cc-221">(16)</span><span class="sxs-lookup"><span data-stu-id="982cc-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-222">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="982cc-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="982cc-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="982cc-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="982cc-224">(17)</span><span class="sxs-lookup"><span data-stu-id="982cc-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-225">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="982cc-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="982cc-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="982cc-227">(18)</span><span class="sxs-lookup"><span data-stu-id="982cc-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-228">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="982cc-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="982cc-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="982cc-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="982cc-230">(19)</span><span class="sxs-lookup"><span data-stu-id="982cc-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="982cc-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="982cc-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="982cc-232">(20)</span><span class="sxs-lookup"><span data-stu-id="982cc-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-233">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="982cc-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="982cc-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="982cc-235">(21)</span><span class="sxs-lookup"><span data-stu-id="982cc-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-236">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="982cc-236">System failure.</span></span> <span data-ttu-id="982cc-237">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="982cc-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="982cc-238">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="982cc-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="982cc-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="982cc-240">(22)</span><span class="sxs-lookup"><span data-stu-id="982cc-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-241">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="982cc-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="982cc-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="982cc-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="982cc-243">(23)</span><span class="sxs-lookup"><span data-stu-id="982cc-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="982cc-244">System failure.</span></span> <span data-ttu-id="982cc-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="982cc-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="982cc-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="982cc-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="982cc-247">(24)</span><span class="sxs-lookup"><span data-stu-id="982cc-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-248">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="982cc-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="982cc-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="982cc-250">(25)</span><span class="sxs-lookup"><span data-stu-id="982cc-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-251">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="982cc-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="982cc-253">(26)</span><span class="sxs-lookup"><span data-stu-id="982cc-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-254">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982cc-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="982cc-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="982cc-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="982cc-256">(27)</span><span class="sxs-lookup"><span data-stu-id="982cc-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-257">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="982cc-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="982cc-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="982cc-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="982cc-259">(28)</span><span class="sxs-lookup"><span data-stu-id="982cc-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-260">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="982cc-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="982cc-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="982cc-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="982cc-262">(29)</span><span class="sxs-lookup"><span data-stu-id="982cc-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-263">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="982cc-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="982cc-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="982cc-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="982cc-265">(30)</span><span class="sxs-lookup"><span data-stu-id="982cc-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-266">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="982cc-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="982cc-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="982cc-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="982cc-268">(31)</span><span class="sxs-lookup"><span data-stu-id="982cc-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-269">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="982cc-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="982cc-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="982cc-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-271">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="982cc-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-273">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="982cc-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-274">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="982cc-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="982cc-275">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="982cc-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-279">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="982cc-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="982cc-280">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="982cc-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="982cc-281">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="982cc-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="982cc-282">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-283">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="982cc-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-286">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="982cc-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-287">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="982cc-287">Textual description of the object.</span></span>

<span data-ttu-id="982cc-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="982cc-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-292">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="982cc-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="982cc-293">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="982cc-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="982cc-294">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-295">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="982cc-295">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-296">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="982cc-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-298">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="982cc-298">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="982cc-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-300">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="982cc-300">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-303">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem tomadas.</span><span class="sxs-lookup"><span data-stu-id="982cc-303">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to take.</span></span>

<span data-ttu-id="982cc-304">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="982cc-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-306">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="982cc-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-308">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="982cc-308">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-309">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="982cc-309">Date and time the object was installed.</span></span> <span data-ttu-id="982cc-310">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="982cc-310">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="982cc-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-312">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="982cc-312">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-313">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="982cc-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-315">Se for **true**, o dispositivo será bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="982cc-315">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="982cc-316">Essa propriedade é herdada [**do \_ userdevice do CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-316">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="982cc-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-318">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="982cc-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-320">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="982cc-320">Last error code reported by the logical device.</span></span>

<span data-ttu-id="982cc-321">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-322">**Layout**</span><span class="sxs-lookup"><span data-stu-id="982cc-322">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-325">Cadeia de caracteres de forma livre que indica o formato e o layout do teclado.</span><span class="sxs-lookup"><span data-stu-id="982cc-325">Free-form string that indicates the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="982cc-326">**Nome**</span><span class="sxs-lookup"><span data-stu-id="982cc-326">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-329">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="982cc-329">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-330">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="982cc-330">Label by which the object is known.</span></span> <span data-ttu-id="982cc-331">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="982cc-331">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="982cc-332">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-333">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="982cc-333">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-334">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982cc-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-336">Número de teclas de função no teclado.</span><span class="sxs-lookup"><span data-stu-id="982cc-336">Number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="982cc-337">**Senha**</span><span class="sxs-lookup"><span data-stu-id="982cc-337">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-338">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982cc-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-340">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Segurança de hardware do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="982cc-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-341">Inteiro que indica se uma senha de nível de hardware está habilitada no teclado para impedir a entrada local.</span><span class="sxs-lookup"><span data-stu-id="982cc-341">Integer that indicates whether a hardware-level password is enabled on the keyboard to prevent local input.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="982cc-342">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="982cc-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="982cc-343">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="982cc-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="982cc-344">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="982cc-344">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="982cc-345">**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="982cc-345">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="982cc-346">**Não implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="982cc-346">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="982cc-347">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="982cc-347">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-350">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="982cc-350">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-351">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="982cc-351">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="982cc-352">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="982cc-352">Example: "\*PNP030b"</span></span>

<span data-ttu-id="982cc-353">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-354">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="982cc-354">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-355">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982cc-355">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="982cc-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-357">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="982cc-357">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="982cc-358">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="982cc-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="982cc-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="982cc-360"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="982cc-360"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="982cc-361"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="982cc-361"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="982cc-362"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="982cc-362"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-363">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="982cc-363">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="982cc-364"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="982cc-364"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-365">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="982cc-365">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="982cc-366"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="982cc-366"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-367">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="982cc-367">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="982cc-368">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="982cc-368">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="982cc-369">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="982cc-369">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="982cc-370"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="982cc-370"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-371">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="982cc-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="982cc-372"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="982cc-372"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="982cc-373">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="982cc-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="982cc-374">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="982cc-374">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-375">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="982cc-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982cc-377">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="982cc-377">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="982cc-378">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="982cc-378">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="982cc-379">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="982cc-379">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="982cc-380">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="982cc-380">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="982cc-381">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-382">**Status**</span><span class="sxs-lookup"><span data-stu-id="982cc-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-383">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-385">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="982cc-385">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-386">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="982cc-386">Current status of the object.</span></span>

<span data-ttu-id="982cc-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="982cc-388">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="982cc-388">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="982cc-389">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="982cc-389">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="982cc-390">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="982cc-390">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="982cc-391">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="982cc-391">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="982cc-392">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="982cc-392">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="982cc-393">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="982cc-393">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="982cc-394">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="982cc-394">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="982cc-395">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="982cc-395">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="982cc-396">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="982cc-396">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="982cc-397">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="982cc-397">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="982cc-398">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="982cc-398">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="982cc-399">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="982cc-399">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="982cc-400">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="982cc-400">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="982cc-401">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="982cc-401">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-402">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982cc-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-404">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="982cc-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="982cc-405">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="982cc-405">State of the logical device.</span></span> <span data-ttu-id="982cc-406">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="982cc-406">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="982cc-407">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="982cc-408">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="982cc-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="982cc-409">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="982cc-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="982cc-410">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="982cc-410">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="982cc-411">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="982cc-411">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="982cc-412">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="982cc-412">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="982cc-413">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="982cc-413">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-414">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-416">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="982cc-416">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="982cc-417">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="982cc-417">Scoping system's creation class name.</span></span>

<span data-ttu-id="982cc-418">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="982cc-419">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="982cc-419">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982cc-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="982cc-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="982cc-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="982cc-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="982cc-422">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="982cc-422">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="982cc-423">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="982cc-423">Scoping system's name.</span></span>

<span data-ttu-id="982cc-424">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="982cc-425">Comentários</span><span class="sxs-lookup"><span data-stu-id="982cc-425">Remarks</span></span>

<span data-ttu-id="982cc-426">A classe de **\_ teclado CIM** é derivada de [**CIM \_ userdevice**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-426">The **CIM\_Keyboard** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="982cc-427">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="982cc-427">WMI does not implement this class.</span></span> <span data-ttu-id="982cc-428">Para classes derivadas do **\_ teclado CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="982cc-428">For classes derived from **CIM\_Keyboard**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="982cc-429">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="982cc-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="982cc-430">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="982cc-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="982cc-431">Requisitos</span><span class="sxs-lookup"><span data-stu-id="982cc-431">Requirements</span></span>



| <span data-ttu-id="982cc-432">Requisito</span><span class="sxs-lookup"><span data-stu-id="982cc-432">Requirement</span></span> | <span data-ttu-id="982cc-433">Valor</span><span class="sxs-lookup"><span data-stu-id="982cc-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="982cc-434">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="982cc-434">Minimum supported client</span></span><br/> | <span data-ttu-id="982cc-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="982cc-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="982cc-436">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="982cc-436">Minimum supported server</span></span><br/> | <span data-ttu-id="982cc-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="982cc-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="982cc-438">Namespace</span><span class="sxs-lookup"><span data-stu-id="982cc-438">Namespace</span></span><br/>                | <span data-ttu-id="982cc-439">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="982cc-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="982cc-440">MOF</span><span class="sxs-lookup"><span data-stu-id="982cc-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="982cc-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="982cc-442">DLL</span><span class="sxs-lookup"><span data-stu-id="982cc-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="982cc-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="982cc-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="982cc-444">Confira também</span><span class="sxs-lookup"><span data-stu-id="982cc-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="982cc-445">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="982cc-445">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

