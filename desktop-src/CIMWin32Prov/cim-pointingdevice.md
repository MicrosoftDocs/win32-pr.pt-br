---
description: A \_ classe CIM PointingDevice representa um dispositivo que aponta para regiões na exibição. Qualquer dispositivo que manipule um ponteiro ou aponta para regiões em uma exibição Visual é membro dessa classe. Por exemplo, um mouse, uma caneta, um touch pad ou um Tablet.
ms.assetid: b093134a-534a-4680-8fce-d96baff26139
ms.tgt_platform: multiple
title: Classe CIM_PointingDevice (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.Availability
- CIM_PointingDevice.Caption
- CIM_PointingDevice.ConfigManagerErrorCode
- CIM_PointingDevice.ConfigManagerUserConfig
- CIM_PointingDevice.CreationClassName
- CIM_PointingDevice.Description
- CIM_PointingDevice.DeviceID
- CIM_PointingDevice.ErrorCleared
- CIM_PointingDevice.ErrorDescription
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.InstallDate
- CIM_PointingDevice.IsLocked
- CIM_PointingDevice.LastErrorCode
- CIM_PointingDevice.Name
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.PNPDeviceID
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.PowerManagementCapabilities
- CIM_PointingDevice.PowerManagementSupported
- CIM_PointingDevice.Resolution
- CIM_PointingDevice.Status
- CIM_PointingDevice.StatusInfo
- CIM_PointingDevice.SystemCreationClassName
- CIM_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3f0a52ac11d927f5cabf171f49fee3a5febaa6a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164129"
---
# <a name="cim_pointingdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="5d713-105">Classe CIM_PointingDevice (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="5d713-105">CIM_PointingDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5d713-106">A classe **CIM \_ PointingDevice** representa um dispositivo que aponta para regiões na exibição.</span><span class="sxs-lookup"><span data-stu-id="5d713-106">The **CIM\_PointingDevice** class represents a device that points to regions on the display.</span></span> <span data-ttu-id="5d713-107">Qualquer dispositivo que manipule um ponteiro ou aponta para regiões em uma exibição Visual é membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5d713-107">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="5d713-108">Por exemplo, um mouse, uma caneta, um touch pad ou um Tablet.</span><span class="sxs-lookup"><span data-stu-id="5d713-108">For example, a mouse, stylus, touch pad, or tablet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d713-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5d713-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d713-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d713-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d713-111">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d713-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5d713-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5d713-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d713-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d713-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C535-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
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
  uint16   Handedness;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="5d713-114">Membros</span><span class="sxs-lookup"><span data-stu-id="5d713-114">Members</span></span>

<span data-ttu-id="5d713-115">A classe **CIM \_ PointingDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d713-115">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5d713-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d713-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="5d713-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d713-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5d713-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d713-118">Methods</span></span>

<span data-ttu-id="5d713-119">A classe **CIM \_ PointingDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5d713-119">The **CIM\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="5d713-120">Método</span><span class="sxs-lookup"><span data-stu-id="5d713-120">Method</span></span>                                                                    | <span data-ttu-id="5d713-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d713-121">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d713-122">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="5d713-122">**Reset**</span></span>](reset-method-in-class-cim-pointingdevice.md)                 | <span data-ttu-id="5d713-123">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d713-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="5d713-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d713-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="5d713-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5d713-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pointingdevice.md) | <span data-ttu-id="5d713-126">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="5d713-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="5d713-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d713-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5d713-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d713-128">Properties</span></span>

<span data-ttu-id="5d713-129">A classe **CIM \_ PointingDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d713-129">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d713-130">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="5d713-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d713-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-133">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5d713-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-134">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-134">Availability and status of the device.</span></span>

<span data-ttu-id="5d713-135">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d713-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5d713-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d713-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5d713-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5d713-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5d713-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5d713-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="5d713-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5d713-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="5d713-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5d713-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="5d713-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5d713-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="5d713-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5d713-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="5d713-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5d713-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="5d713-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5d713-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5d713-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5d713-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5d713-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5d713-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="5d713-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5d713-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="5d713-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-149">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5d713-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5d713-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="5d713-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-151">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="5d713-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5d713-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5d713-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-153">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5d713-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="5d713-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5d713-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="5d713-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-156">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5d713-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5d713-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5d713-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-158">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="5d713-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5d713-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="5d713-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-160">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="5d713-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5d713-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5d713-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-162">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="5d713-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5d713-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="5d713-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-164">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="5d713-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5d713-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-168">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5d713-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-169">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d713-169">Short textual description of the object.</span></span>

<span data-ttu-id="5d713-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5d713-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d713-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-174">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5d713-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-175">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5d713-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5d713-176">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5d713-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5d713-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5d713-178"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="5d713-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-179">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5d713-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5d713-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5d713-181">(1)</span><span class="sxs-lookup"><span data-stu-id="5d713-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-182">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5d713-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5d713-184">(2)</span><span class="sxs-lookup"><span data-stu-id="5d713-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5d713-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5d713-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5d713-186">(3)</span><span class="sxs-lookup"><span data-stu-id="5d713-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-187">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="5d713-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5d713-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5d713-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5d713-189">(4)</span><span class="sxs-lookup"><span data-stu-id="5d713-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-190">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-190">Device is not working properly.</span></span> <span data-ttu-id="5d713-191">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5d713-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5d713-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="5d713-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5d713-193">(5)</span><span class="sxs-lookup"><span data-stu-id="5d713-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-194">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="5d713-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5d713-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5d713-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5d713-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="5d713-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-197">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5d713-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5d713-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5d713-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5d713-199">(7)</span><span class="sxs-lookup"><span data-stu-id="5d713-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5d713-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="5d713-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5d713-201">(8)</span><span class="sxs-lookup"><span data-stu-id="5d713-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-202">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="5d713-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5d713-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="5d713-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5d713-204">(9)</span><span class="sxs-lookup"><span data-stu-id="5d713-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-205">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-205">Device is not working properly.</span></span> <span data-ttu-id="5d713-206">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5d713-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="5d713-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5d713-208">(10)</span><span class="sxs-lookup"><span data-stu-id="5d713-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-209">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5d713-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="5d713-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5d713-211">(11)</span><span class="sxs-lookup"><span data-stu-id="5d713-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-212">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5d713-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="5d713-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5d713-214">12</span><span class="sxs-lookup"><span data-stu-id="5d713-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-215">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="5d713-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5d713-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5d713-217">(13)</span><span class="sxs-lookup"><span data-stu-id="5d713-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-218">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5d713-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="5d713-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5d713-220">(14)</span><span class="sxs-lookup"><span data-stu-id="5d713-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-221">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5d713-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5d713-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="5d713-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5d713-223">(15)</span><span class="sxs-lookup"><span data-stu-id="5d713-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-224">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="5d713-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5d713-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="5d713-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5d713-226">(16)</span><span class="sxs-lookup"><span data-stu-id="5d713-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-227">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="5d713-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5d713-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="5d713-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5d713-229">(17)</span><span class="sxs-lookup"><span data-stu-id="5d713-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-230">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5d713-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5d713-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5d713-232">(18)</span><span class="sxs-lookup"><span data-stu-id="5d713-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-233">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="5d713-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5d713-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="5d713-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5d713-235">(19)</span><span class="sxs-lookup"><span data-stu-id="5d713-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5d713-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5d713-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5d713-237">(20)</span><span class="sxs-lookup"><span data-stu-id="5d713-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-238">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5d713-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5d713-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5d713-240">(21)</span><span class="sxs-lookup"><span data-stu-id="5d713-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-241">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d713-241">System failure.</span></span> <span data-ttu-id="5d713-242">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5d713-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5d713-243">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5d713-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5d713-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5d713-245">(22)</span><span class="sxs-lookup"><span data-stu-id="5d713-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-246">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5d713-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5d713-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="5d713-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5d713-248">(23)</span><span class="sxs-lookup"><span data-stu-id="5d713-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-249">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d713-249">System failure.</span></span> <span data-ttu-id="5d713-250">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5d713-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5d713-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="5d713-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5d713-252">(24)</span><span class="sxs-lookup"><span data-stu-id="5d713-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-253">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="5d713-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5d713-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5d713-255">(25)</span><span class="sxs-lookup"><span data-stu-id="5d713-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-256">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5d713-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5d713-258">(26)</span><span class="sxs-lookup"><span data-stu-id="5d713-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d713-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5d713-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="5d713-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5d713-261">(27)</span><span class="sxs-lookup"><span data-stu-id="5d713-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-262">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="5d713-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5d713-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="5d713-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5d713-264">(28)</span><span class="sxs-lookup"><span data-stu-id="5d713-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-265">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="5d713-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5d713-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="5d713-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5d713-267">(29)</span><span class="sxs-lookup"><span data-stu-id="5d713-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-268">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5d713-268">Device is disabled.</span></span> <span data-ttu-id="5d713-269">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="5d713-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5d713-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5d713-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5d713-271">(30)</span><span class="sxs-lookup"><span data-stu-id="5d713-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-272">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5d713-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5d713-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d713-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5d713-274">(31)</span><span class="sxs-lookup"><span data-stu-id="5d713-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-275">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-275">Device is not working properly.</span></span> <span data-ttu-id="5d713-276">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="5d713-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5d713-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-278">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d713-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-280">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5d713-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-281">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5d713-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5d713-282">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d713-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-286">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d713-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d713-287">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5d713-287">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5d713-288">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5d713-288">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5d713-289">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-290">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d713-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-293">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5d713-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-294">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d713-294">Textual description of the object.</span></span>

<span data-ttu-id="5d713-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5d713-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-299">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d713-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d713-300">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d713-300">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5d713-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5d713-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-303">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d713-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-305">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="5d713-305">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5d713-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5d713-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-310">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="5d713-310">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5d713-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-312">**Direção**</span><span class="sxs-lookup"><span data-stu-id="5d713-312">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-313">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d713-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-315">Configuração do dispositivo apontador para a operação do lado direito ou esquerdo.</span><span class="sxs-lookup"><span data-stu-id="5d713-315">Configuration of the pointing device for right-hand or left-hand operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d713-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5d713-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5d713-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (1)</span><span class="sxs-lookup"><span data-stu-id="5d713-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="5d713-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Operação da mão direita** (2)</span><span class="sxs-lookup"><span data-stu-id="5d713-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-319">Operação do lado direito</span><span class="sxs-lookup"><span data-stu-id="5d713-319">Right-hand operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="5d713-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Operação da mão esquerda** (3)</span><span class="sxs-lookup"><span data-stu-id="5d713-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-321">Operação do lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="5d713-321">Left-hand operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5d713-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-323">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d713-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-325">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5d713-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-326">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5d713-326">Date and time the object was installed.</span></span> <span data-ttu-id="5d713-327">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5d713-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5d713-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-329">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="5d713-329">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-330">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d713-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-332">Se for **true**, o dispositivo será bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d713-332">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="5d713-333">Essa propriedade é herdada [**do \_ userdevice do CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-333">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5d713-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d713-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-337">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d713-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5d713-338">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-339">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5d713-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-342">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5d713-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-343">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5d713-343">Label by which the object is known.</span></span> <span data-ttu-id="5d713-344">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5d713-344">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5d713-345">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-345">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-346">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="5d713-346">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-347">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5d713-347">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-349">Número de botões no dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="5d713-349">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="5d713-350">Exemplo: "2"</span><span class="sxs-lookup"><span data-stu-id="5d713-350">Example: "2"</span></span>

</dd> <dt>

<span data-ttu-id="5d713-351">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5d713-351">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-354">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5d713-354">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-355">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d713-355">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="5d713-356">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5d713-357">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5d713-357">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5d713-358">**Ponto de apontar**</span><span class="sxs-lookup"><span data-stu-id="5d713-358">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-359">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d713-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-361">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo apontador DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="5d713-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-362">Tipo do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="5d713-362">Type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d713-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5d713-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d713-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5d713-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="5d713-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="5d713-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="5d713-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Rastrear bola** (4)</span><span class="sxs-lookup"><span data-stu-id="5d713-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-367">Ficar</span><span class="sxs-lookup"><span data-stu-id="5d713-367">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="5d713-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Ponto de controle** (5)</span><span class="sxs-lookup"><span data-stu-id="5d713-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="5d713-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Ponto de deslizamento** (6)</span><span class="sxs-lookup"><span data-stu-id="5d713-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="5d713-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch pad** (7)</span><span class="sxs-lookup"><span data-stu-id="5d713-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="5d713-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Tela sensível ao toque** (8)</span><span class="sxs-lookup"><span data-stu-id="5d713-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="5d713-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Sensor de mouse-óptico** (9)</span><span class="sxs-lookup"><span data-stu-id="5d713-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-373">Sensor óptico do mouse</span><span class="sxs-lookup"><span data-stu-id="5d713-373">Mouse   optical sensor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5d713-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-375">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d713-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5d713-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-377">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d713-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5d713-378">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="5d713-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d713-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5d713-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5d713-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5d713-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5d713-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5d713-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5d713-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5d713-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-383">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5d713-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5d713-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5d713-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-385">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="5d713-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5d713-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="5d713-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-387">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5d713-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5d713-388">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="5d713-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5d713-389">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5d713-389">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5d713-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="5d713-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-391">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="5d713-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5d713-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="5d713-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5d713-393">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="5d713-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-394">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5d713-394">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-395">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d713-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d713-397">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5d713-397">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5d713-398">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5d713-398">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5d713-399">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="5d713-399">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5d713-400">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5d713-400">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="5d713-401">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-402">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="5d713-402">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-403">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d713-403">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-405">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagens por polegada")</span><span class="sxs-lookup"><span data-stu-id="5d713-405">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-406">Resolução de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="5d713-406">Tracking resolution.</span></span>

<span data-ttu-id="5d713-407">Exemplo: "0"</span><span class="sxs-lookup"><span data-stu-id="5d713-407">Example: "0"</span></span>

</dd> <dt>

<span data-ttu-id="5d713-408">**Status**</span><span class="sxs-lookup"><span data-stu-id="5d713-408">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-411">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5d713-411">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-412">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d713-412">Current status of the object.</span></span> <span data-ttu-id="5d713-413">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5d713-414">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5d713-414">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5d713-415">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5d713-415">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5d713-416">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5d713-416">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5d713-417">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5d713-417">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d713-418">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5d713-418">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5d713-419">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5d713-419">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5d713-420">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5d713-420">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5d713-421">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5d713-421">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5d713-422">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5d713-422">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5d713-423">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5d713-423">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5d713-424">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5d713-424">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5d713-425">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5d713-425">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5d713-426">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5d713-426">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-427">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5d713-427">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-428">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d713-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-430">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="5d713-430">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5d713-431">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d713-431">State of the logical device.</span></span> <span data-ttu-id="5d713-432">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="5d713-432">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5d713-433">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d713-434">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5d713-434">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d713-435">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5d713-435">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5d713-436">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5d713-436">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5d713-437">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5d713-437">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5d713-438">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="5d713-438">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d713-439">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d713-439">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-442">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d713-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d713-443">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5d713-443">Scoping system's creation class name.</span></span>

<span data-ttu-id="5d713-444">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d713-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5d713-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d713-446">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d713-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d713-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d713-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d713-448">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d713-448">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d713-449">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5d713-449">Scoping system's name.</span></span>

<span data-ttu-id="5d713-450">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d713-451">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d713-451">Remarks</span></span>

<span data-ttu-id="5d713-452">A classe **CIM \_ PointingDevice** é derivada de [**\_ userdevice do CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-452">The **CIM\_PointingDevice** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="5d713-453">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5d713-453">WMI does not implement this class.</span></span> <span data-ttu-id="5d713-454">Para classes WMI derivadas do **CIM \_ PointingDevice**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5d713-454">For WMI classes derived from **CIM\_PointingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5d713-455">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d713-455">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d713-456">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5d713-456">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d713-457">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d713-457">Requirements</span></span>



| <span data-ttu-id="5d713-458">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d713-458">Requirement</span></span> | <span data-ttu-id="5d713-459">Valor</span><span class="sxs-lookup"><span data-stu-id="5d713-459">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d713-460">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d713-460">Minimum supported client</span></span><br/> | <span data-ttu-id="5d713-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d713-461">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d713-462">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d713-462">Minimum supported server</span></span><br/> | <span data-ttu-id="5d713-463">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d713-463">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d713-464">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d713-464">Namespace</span></span><br/>                | <span data-ttu-id="5d713-465">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5d713-465">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d713-466">MOF</span><span class="sxs-lookup"><span data-stu-id="5d713-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d713-467"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d713-467"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d713-468">DLL</span><span class="sxs-lookup"><span data-stu-id="5d713-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d713-469"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d713-469"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d713-470">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d713-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d713-471">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5d713-471">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

