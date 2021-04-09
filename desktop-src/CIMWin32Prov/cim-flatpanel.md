---
description: A \_ classe CIM FlatPanel representa os recursos e o gerenciamento do dispositivo lógico do painel plano.
ms.assetid: 0c515621-4ff9-42af-a281-ac49af6d96ba
ms.tgt_platform: multiple
title: Classe CIM_FlatPanel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel
- CIM_FlatPanel.Availability
- CIM_FlatPanel.Caption
- CIM_FlatPanel.ConfigManagerErrorCode
- CIM_FlatPanel.ConfigManagerUserConfig
- CIM_FlatPanel.CreationClassName
- CIM_FlatPanel.Description
- CIM_FlatPanel.DeviceID
- CIM_FlatPanel.DisplayType
- CIM_FlatPanel.ErrorCleared
- CIM_FlatPanel.ErrorDescription
- CIM_FlatPanel.HorizontalResolution
- CIM_FlatPanel.InstallDate
- CIM_FlatPanel.IsLocked
- CIM_FlatPanel.LastErrorCode
- CIM_FlatPanel.LightSource
- CIM_FlatPanel.Name
- CIM_FlatPanel.PNPDeviceID
- CIM_FlatPanel.PowerManagementCapabilities
- CIM_FlatPanel.PowerManagementSupported
- CIM_FlatPanel.ScanMode
- CIM_FlatPanel.Status
- CIM_FlatPanel.StatusInfo
- CIM_FlatPanel.SupportsColor
- CIM_FlatPanel.SystemCreationClassName
- CIM_FlatPanel.SystemName
- CIM_FlatPanel.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c399383223734d2f8ebe68528352c229a74bfbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920386"
---
# <a name="cim_flatpanel-class"></a><span data-ttu-id="34d58-103">\_Classe CIM FlatPanel</span><span class="sxs-lookup"><span data-stu-id="34d58-103">CIM\_FlatPanel class</span></span>

<span data-ttu-id="34d58-104">A classe **CIM \_ FlatPanel** representa os recursos e o gerenciamento do dispositivo lógico do painel plano.</span><span class="sxs-lookup"><span data-stu-id="34d58-104">The **CIM\_FlatPanel** class represents the capabilities and management of the flat panel logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34d58-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="34d58-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="34d58-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="34d58-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="34d58-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="34d58-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="34d58-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="34d58-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d58-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34d58-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE9-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_FlatPanel : CIM_Display
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   HorizontalResolution;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  uint16   LightSource;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ScanMode;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsColor;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="34d58-110">Membros</span><span class="sxs-lookup"><span data-stu-id="34d58-110">Members</span></span>

<span data-ttu-id="34d58-111">A classe **CIM \_ FlatPanel** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="34d58-111">The **CIM\_FlatPanel** class has these types of members:</span></span>

-   [<span data-ttu-id="34d58-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="34d58-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="34d58-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34d58-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34d58-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="34d58-114">Methods</span></span>

<span data-ttu-id="34d58-115">A classe **CIM \_ FlatPanel** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="34d58-115">The **CIM\_FlatPanel** class has these methods.</span></span>



| <span data-ttu-id="34d58-116">Método</span><span class="sxs-lookup"><span data-stu-id="34d58-116">Method</span></span>                                                               | <span data-ttu-id="34d58-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="34d58-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34d58-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="34d58-118">**Reset**</span></span>](reset-method-in-class-cim-flatpanel.md)                 | <span data-ttu-id="34d58-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34d58-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="34d58-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="34d58-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="34d58-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="34d58-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-flatpanel.md) | <span data-ttu-id="34d58-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="34d58-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="34d58-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="34d58-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="34d58-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34d58-124">Properties</span></span>

<span data-ttu-id="34d58-125">A classe **CIM \_ FlatPanel** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="34d58-125">The **CIM\_FlatPanel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34d58-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="34d58-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d58-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="34d58-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-130">Availability and status of the device.</span></span>

<span data-ttu-id="34d58-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34d58-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34d58-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="34d58-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="34d58-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="34d58-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="34d58-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="34d58-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="34d58-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="34d58-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="34d58-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="34d58-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="34d58-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="34d58-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="34d58-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="34d58-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="34d58-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="34d58-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="34d58-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="34d58-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="34d58-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="34d58-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="34d58-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="34d58-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="34d58-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="34d58-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="34d58-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="34d58-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="34d58-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="34d58-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="34d58-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="34d58-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="34d58-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="34d58-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="34d58-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="34d58-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="34d58-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="34d58-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="34d58-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="34d58-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="34d58-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="34d58-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="34d58-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="34d58-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="34d58-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="34d58-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="34d58-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="34d58-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="34d58-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="34d58-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-161">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="34d58-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-164">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="34d58-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-165">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="34d58-165">Short textual description of the object.</span></span>

<span data-ttu-id="34d58-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="34d58-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34d58-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-170">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="34d58-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-171">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="34d58-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="34d58-172">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="34d58-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="34d58-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="34d58-174"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="34d58-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-175">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="34d58-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="34d58-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="34d58-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="34d58-177">(1)</span><span class="sxs-lookup"><span data-stu-id="34d58-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-178">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="34d58-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="34d58-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="34d58-180">(2)</span><span class="sxs-lookup"><span data-stu-id="34d58-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="34d58-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="34d58-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="34d58-182">(3)</span><span class="sxs-lookup"><span data-stu-id="34d58-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-183">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="34d58-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="34d58-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="34d58-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="34d58-185">(4)</span><span class="sxs-lookup"><span data-stu-id="34d58-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-186">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="34d58-186">Device is not working properly.</span></span> <span data-ttu-id="34d58-187">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="34d58-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="34d58-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="34d58-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="34d58-189">(5)</span><span class="sxs-lookup"><span data-stu-id="34d58-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-190">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="34d58-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="34d58-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="34d58-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="34d58-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="34d58-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-193">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="34d58-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="34d58-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="34d58-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="34d58-195">(7)</span><span class="sxs-lookup"><span data-stu-id="34d58-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="34d58-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="34d58-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="34d58-197">(8)</span><span class="sxs-lookup"><span data-stu-id="34d58-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-198">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="34d58-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="34d58-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="34d58-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="34d58-200">(9)</span><span class="sxs-lookup"><span data-stu-id="34d58-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-201">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="34d58-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="34d58-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="34d58-203">(10)</span><span class="sxs-lookup"><span data-stu-id="34d58-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-204">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="34d58-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="34d58-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="34d58-206">(11)</span><span class="sxs-lookup"><span data-stu-id="34d58-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-207">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="34d58-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="34d58-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="34d58-209">12</span><span class="sxs-lookup"><span data-stu-id="34d58-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-210">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="34d58-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="34d58-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="34d58-212">(13)</span><span class="sxs-lookup"><span data-stu-id="34d58-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-213">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="34d58-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="34d58-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="34d58-215">(14)</span><span class="sxs-lookup"><span data-stu-id="34d58-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-216">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="34d58-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="34d58-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="34d58-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="34d58-218">(15)</span><span class="sxs-lookup"><span data-stu-id="34d58-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-219">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="34d58-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="34d58-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="34d58-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="34d58-221">(16)</span><span class="sxs-lookup"><span data-stu-id="34d58-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-222">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="34d58-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="34d58-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="34d58-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="34d58-224">(17)</span><span class="sxs-lookup"><span data-stu-id="34d58-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-225">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="34d58-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="34d58-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="34d58-227">(18)</span><span class="sxs-lookup"><span data-stu-id="34d58-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-228">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="34d58-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="34d58-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="34d58-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="34d58-230">(19)</span><span class="sxs-lookup"><span data-stu-id="34d58-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="34d58-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="34d58-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="34d58-232">(20)</span><span class="sxs-lookup"><span data-stu-id="34d58-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-233">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="34d58-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="34d58-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="34d58-235">(21)</span><span class="sxs-lookup"><span data-stu-id="34d58-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-236">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="34d58-236">System failure.</span></span> <span data-ttu-id="34d58-237">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="34d58-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="34d58-238">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="34d58-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="34d58-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="34d58-240">(22)</span><span class="sxs-lookup"><span data-stu-id="34d58-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-241">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="34d58-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="34d58-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="34d58-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="34d58-243">(23)</span><span class="sxs-lookup"><span data-stu-id="34d58-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="34d58-244">System failure.</span></span> <span data-ttu-id="34d58-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="34d58-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="34d58-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="34d58-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="34d58-247">(24)</span><span class="sxs-lookup"><span data-stu-id="34d58-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-248">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="34d58-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="34d58-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="34d58-250">(25)</span><span class="sxs-lookup"><span data-stu-id="34d58-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-251">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="34d58-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="34d58-253">(26)</span><span class="sxs-lookup"><span data-stu-id="34d58-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-254">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d58-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="34d58-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="34d58-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="34d58-256">(27)</span><span class="sxs-lookup"><span data-stu-id="34d58-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-257">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="34d58-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="34d58-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="34d58-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="34d58-259">(28)</span><span class="sxs-lookup"><span data-stu-id="34d58-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-260">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="34d58-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="34d58-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="34d58-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="34d58-262">(29)</span><span class="sxs-lookup"><span data-stu-id="34d58-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-263">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="34d58-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="34d58-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="34d58-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="34d58-265">(30)</span><span class="sxs-lookup"><span data-stu-id="34d58-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-266">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="34d58-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="34d58-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34d58-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="34d58-268">(31)</span><span class="sxs-lookup"><span data-stu-id="34d58-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-269">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="34d58-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="34d58-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-271">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34d58-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-273">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="34d58-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-274">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="34d58-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="34d58-275">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34d58-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-279">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34d58-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34d58-280">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="34d58-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="34d58-281">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="34d58-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="34d58-282">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-283">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34d58-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-286">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="34d58-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-287">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="34d58-287">Textual description of the object.</span></span>

<span data-ttu-id="34d58-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="34d58-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-292">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34d58-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34d58-293">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34d58-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="34d58-294">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-295">**TipoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="34d58-295">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-296">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d58-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-298">Enumeração que descreve o tipo de exibição de tela plana.</span><span class="sxs-lookup"><span data-stu-id="34d58-298">Enumeration that describes the type of flat panel display.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="34d58-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34d58-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34d58-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>

<span data-ttu-id="34d58-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**LCD de matriz passiva** (2)</span><span class="sxs-lookup"><span data-stu-id="34d58-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**Passive Matrix LCD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>

<span data-ttu-id="34d58-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**LCD de matriz ativa** (3)</span><span class="sxs-lookup"><span data-stu-id="34d58-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**Active Matrix LCD** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>

<span data-ttu-id="34d58-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**LCD Cholesteric** (4)</span><span class="sxs-lookup"><span data-stu-id="34d58-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**Cholesteric LCD** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>

<span data-ttu-id="34d58-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Exibição de emissão de campo** (5)</span><span class="sxs-lookup"><span data-stu-id="34d58-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Field Emission Display** (5)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-305">Emissão de campo</span><span class="sxs-lookup"><span data-stu-id="34d58-305">Field emission</span></span>

</dd> <dt>

<span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>

<span data-ttu-id="34d58-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Tela de luminescent de eletromagnético** (6)</span><span class="sxs-lookup"><span data-stu-id="34d58-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Electro Luminescent Display** (6)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-307">Luminescent de eletromagnético</span><span class="sxs-lookup"><span data-stu-id="34d58-307">Electro luminescent</span></span>

</dd> <dt>

<span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>

<span data-ttu-id="34d58-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Plasma de gás** (7)</span><span class="sxs-lookup"><span data-stu-id="34d58-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Gas Plasma** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="LED"></span><span id="led"></span>

<span data-ttu-id="34d58-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span><span class="sxs-lookup"><span data-stu-id="34d58-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="34d58-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-311">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34d58-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-313">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="34d58-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="34d58-314">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="34d58-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-318">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="34d58-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="34d58-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-320">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="34d58-320">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-321">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34d58-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-323">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="34d58-323">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-324">Resolução horizontal, em pixels.</span><span class="sxs-lookup"><span data-stu-id="34d58-324">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="34d58-325">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="34d58-325">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-326">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="34d58-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-328">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="34d58-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-329">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="34d58-329">Date and time the object was installed.</span></span> <span data-ttu-id="34d58-330">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="34d58-330">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="34d58-331">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-332">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="34d58-332">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-333">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34d58-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-335">Se for **true**, o dispositivo será bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="34d58-335">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="34d58-336">Essa propriedade é herdada [**do \_ userdevice do CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-336">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="34d58-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-338">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34d58-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-340">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34d58-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="34d58-341">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-342">**Claridade**</span><span class="sxs-lookup"><span data-stu-id="34d58-342">**LightSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-343">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d58-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-345">Descrição do tipo de iluminação de exibição.</span><span class="sxs-lookup"><span data-stu-id="34d58-345">Description of the display illumination type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-346">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="34d58-346">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34d58-347">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34d58-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Backlit"></span><span id="backlit"></span><span id="BACKLIT"></span>

<span data-ttu-id="34d58-348">**Backlit** (2)</span><span class="sxs-lookup"><span data-stu-id="34d58-348">**Backlit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Edgelit"></span><span id="edgelit"></span><span id="EDGELIT"></span>

<span data-ttu-id="34d58-349">**Edgelit** (3)</span><span class="sxs-lookup"><span data-stu-id="34d58-349">**Edgelit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reflective"></span><span id="reflective"></span><span id="REFLECTIVE"></span>

<span data-ttu-id="34d58-350">**Reflexivo** (4)</span><span class="sxs-lookup"><span data-stu-id="34d58-350">**Reflective** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-351">**Nome**</span><span class="sxs-lookup"><span data-stu-id="34d58-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-354">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="34d58-354">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-355">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="34d58-355">Label by which the object is known.</span></span> <span data-ttu-id="34d58-356">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="34d58-356">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="34d58-357">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-357">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-358">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="34d58-358">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-359">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-361">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="34d58-361">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-362">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34d58-362">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="34d58-363">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="34d58-364">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="34d58-364">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="34d58-365">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="34d58-365">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-366">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d58-366">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34d58-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-368">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34d58-368">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="34d58-369">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="34d58-369">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="34d58-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="34d58-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="34d58-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="34d58-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="34d58-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="34d58-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="34d58-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-374">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="34d58-374">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="34d58-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="34d58-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-376">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="34d58-376">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="34d58-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="34d58-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-378">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="34d58-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="34d58-379">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="34d58-379">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="34d58-380">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="34d58-380">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="34d58-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="34d58-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-382">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="34d58-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="34d58-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="34d58-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="34d58-384">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="34d58-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="34d58-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-386">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34d58-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-388">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="34d58-388">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="34d58-389">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="34d58-389">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="34d58-390">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="34d58-390">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="34d58-391">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="34d58-391">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="34d58-392">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-393">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="34d58-393">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-394">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d58-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-396">Modo de verificação que indica verificação única ou dupla, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="34d58-396">Scan mode that indicates single or dual scan, for example.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-397">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="34d58-397">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34d58-398">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34d58-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Single_Scan"></span><span id="single_scan"></span><span id="SINGLE_SCAN"></span>

<span data-ttu-id="34d58-399">**Verificação única** (2)</span><span class="sxs-lookup"><span data-stu-id="34d58-399">**Single Scan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual_Scan"></span><span id="dual_scan"></span><span id="DUAL_SCAN"></span>

<span data-ttu-id="34d58-400">**Verificação dupla** (3)</span><span class="sxs-lookup"><span data-stu-id="34d58-400">**Dual Scan** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-401">**Status**</span><span class="sxs-lookup"><span data-stu-id="34d58-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-402">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-404">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="34d58-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-405">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="34d58-405">Current status of the object.</span></span> <span data-ttu-id="34d58-406">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="34d58-407">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="34d58-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="34d58-408">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="34d58-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="34d58-409">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="34d58-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="34d58-410">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="34d58-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-411">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="34d58-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="34d58-412">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="34d58-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="34d58-413">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="34d58-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="34d58-414">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="34d58-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="34d58-415">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="34d58-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="34d58-416">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="34d58-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="34d58-417">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="34d58-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="34d58-418">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="34d58-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="34d58-419">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="34d58-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="34d58-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-421">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34d58-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-423">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="34d58-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-424">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34d58-424">State of the logical device.</span></span> <span data-ttu-id="34d58-425">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="34d58-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="34d58-426">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34d58-427">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34d58-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34d58-428">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="34d58-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="34d58-429">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="34d58-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="34d58-430">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="34d58-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="34d58-431">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="34d58-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34d58-432">**SupportsColor**</span><span class="sxs-lookup"><span data-stu-id="34d58-432">**SupportsColor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-433">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34d58-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34d58-435">Se **for true**, o painel Flat oferecerá suporte à exibição de cores.</span><span class="sxs-lookup"><span data-stu-id="34d58-435">If **TRUE**, the flat panel supports color display.</span></span>

</dd> <dt>

<span data-ttu-id="34d58-436">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34d58-436">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-437">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-439">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34d58-439">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34d58-440">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="34d58-440">Scoping system's creation class name.</span></span>

<span data-ttu-id="34d58-441">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-442">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="34d58-442">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34d58-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-445">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34d58-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34d58-446">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="34d58-446">Scoping system's name.</span></span>

<span data-ttu-id="34d58-447">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d58-448">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="34d58-448">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34d58-449">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34d58-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34d58-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34d58-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34d58-451">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="34d58-451">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="34d58-452">Resolução vertical, em pixels.</span><span class="sxs-lookup"><span data-stu-id="34d58-452">Vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34d58-453">Comentários</span><span class="sxs-lookup"><span data-stu-id="34d58-453">Remarks</span></span>

<span data-ttu-id="34d58-454">A classe **CIM \_ FlatPanel** é derivada da [**\_ exibição de CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="34d58-454">The **CIM\_FlatPanel** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="34d58-455">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="34d58-455">WMI does not implement this class.</span></span>

<span data-ttu-id="34d58-456">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="34d58-456">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="34d58-457">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="34d58-457">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d58-458">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34d58-458">Requirements</span></span>



| <span data-ttu-id="34d58-459">Requisito</span><span class="sxs-lookup"><span data-stu-id="34d58-459">Requirement</span></span> | <span data-ttu-id="34d58-460">Valor</span><span class="sxs-lookup"><span data-stu-id="34d58-460">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34d58-461">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34d58-461">Minimum supported client</span></span><br/> | <span data-ttu-id="34d58-462">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34d58-462">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34d58-463">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34d58-463">Minimum supported server</span></span><br/> | <span data-ttu-id="34d58-464">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34d58-464">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34d58-465">Namespace</span><span class="sxs-lookup"><span data-stu-id="34d58-465">Namespace</span></span><br/>                | <span data-ttu-id="34d58-466">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="34d58-466">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34d58-467">MOF</span><span class="sxs-lookup"><span data-stu-id="34d58-467">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34d58-468"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34d58-468"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34d58-469">DLL</span><span class="sxs-lookup"><span data-stu-id="34d58-469">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34d58-470"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34d58-470"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d58-471">Confira também</span><span class="sxs-lookup"><span data-stu-id="34d58-471">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d58-472">**Exibição de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="34d58-472">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

