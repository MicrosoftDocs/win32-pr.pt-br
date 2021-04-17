---
description: A \_ classe CIM SCSIController representa os recursos e o gerenciamento do dispositivo lógico do controlador SCSI.
ms.assetid: a9b3dee4-1e42-4ac3-8c67-1da46f8acb43
ms.tgt_platform: multiple
title: Classe CIM_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIController
- CIM_SCSIController.Availability
- CIM_SCSIController.Caption
- CIM_SCSIController.ConfigManagerErrorCode
- CIM_SCSIController.ConfigManagerUserConfig
- CIM_SCSIController.ControllerTimeouts
- CIM_SCSIController.CreationClassName
- CIM_SCSIController.Description
- CIM_SCSIController.DeviceID
- CIM_SCSIController.ErrorCleared
- CIM_SCSIController.ErrorDescription
- CIM_SCSIController.InstallDate
- CIM_SCSIController.LastErrorCode
- CIM_SCSIController.MaxDataWidth
- CIM_SCSIController.MaxNumberControlled
- CIM_SCSIController.MaxTransferRate
- CIM_SCSIController.Name
- CIM_SCSIController.PNPDeviceID
- CIM_SCSIController.PowerManagementCapabilities
- CIM_SCSIController.PowerManagementSupported
- CIM_SCSIController.ProtectionManagement
- CIM_SCSIController.ProtocolSupported
- CIM_SCSIController.Status
- CIM_SCSIController.StatusInfo
- CIM_SCSIController.SystemCreationClassName
- CIM_SCSIController.SystemName
- CIM_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0523f436081a8b09f562d19d1d337fc1b7574b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762770"
---
# <a name="cim_scsicontroller-class"></a><span data-ttu-id="78b47-103">\_Classe CIM SCSIController</span><span class="sxs-lookup"><span data-stu-id="78b47-103">CIM\_SCSIController class</span></span>

<span data-ttu-id="78b47-104">A classe **CIM \_ SCSIController** representa os recursos e o gerenciamento do dispositivo lógico do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="78b47-104">The **CIM\_SCSIController** class represents the capabilities and management of the SCSI controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78b47-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="78b47-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="78b47-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="78b47-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="78b47-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="78b47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="78b47-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="78b47-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b47-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78b47-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C553-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SCSIController : CIM_Controller
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="78b47-110">Membros</span><span class="sxs-lookup"><span data-stu-id="78b47-110">Members</span></span>

<span data-ttu-id="78b47-111">A classe **CIM \_ SCSIController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="78b47-111">The **CIM\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="78b47-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="78b47-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="78b47-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78b47-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78b47-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="78b47-114">Methods</span></span>

<span data-ttu-id="78b47-115">A classe **CIM \_ SCSIController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="78b47-115">The **CIM\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="78b47-116">Método</span><span class="sxs-lookup"><span data-stu-id="78b47-116">Method</span></span>                                                                    | <span data-ttu-id="78b47-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="78b47-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78b47-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="78b47-118">**Reset**</span></span>](reset-method-in-class-cim-scsicontroller.md)                 | <span data-ttu-id="78b47-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78b47-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="78b47-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="78b47-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="78b47-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="78b47-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-scsicontroller.md) | <span data-ttu-id="78b47-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="78b47-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="78b47-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="78b47-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="78b47-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78b47-124">Properties</span></span>

<span data-ttu-id="78b47-125">A classe **CIM \_ SCSIController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="78b47-125">The **CIM\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78b47-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="78b47-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78b47-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="78b47-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-130">Availability and status of the device.</span></span>

<span data-ttu-id="78b47-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78b47-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78b47-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78b47-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78b47-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="78b47-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="78b47-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-135">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="78b47-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="78b47-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="78b47-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="78b47-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="78b47-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="78b47-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="78b47-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="78b47-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="78b47-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="78b47-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="78b47-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="78b47-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="78b47-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78b47-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="78b47-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="78b47-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="78b47-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="78b47-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="78b47-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="78b47-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="78b47-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-146">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78b47-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="78b47-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="78b47-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-148">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="78b47-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="78b47-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="78b47-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-150">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="78b47-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="78b47-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="78b47-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="78b47-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-153">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="78b47-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="78b47-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="78b47-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-155">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="78b47-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="78b47-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="78b47-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-157">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="78b47-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="78b47-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="78b47-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-159">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="78b47-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="78b47-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="78b47-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-161">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="78b47-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-162">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="78b47-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-165">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="78b47-165">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-166">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="78b47-166">Short textual description of the object.</span></span>

<span data-ttu-id="78b47-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-168">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="78b47-168">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-169">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78b47-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-171">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="78b47-171">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-172">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="78b47-172">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="78b47-173">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-173">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="78b47-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="78b47-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="78b47-175"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="78b47-175">(0)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-176">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-176">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="78b47-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="78b47-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="78b47-178">(1)</span><span class="sxs-lookup"><span data-stu-id="78b47-178">(1)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-179">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-179">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78b47-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="78b47-181">(2)</span><span class="sxs-lookup"><span data-stu-id="78b47-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="78b47-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="78b47-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="78b47-183">(3)</span><span class="sxs-lookup"><span data-stu-id="78b47-183">(3)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-184">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="78b47-184">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="78b47-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="78b47-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="78b47-186">(4)</span><span class="sxs-lookup"><span data-stu-id="78b47-186">(4)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-187">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-187">Device is not working properly.</span></span> <span data-ttu-id="78b47-188">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="78b47-188">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="78b47-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="78b47-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="78b47-190">(5)</span><span class="sxs-lookup"><span data-stu-id="78b47-190">(5)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-191">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="78b47-191">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="78b47-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="78b47-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="78b47-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="78b47-193">(6)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-194">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="78b47-194">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="78b47-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="78b47-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="78b47-196">(7)</span><span class="sxs-lookup"><span data-stu-id="78b47-196">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="78b47-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="78b47-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="78b47-198">(8)</span><span class="sxs-lookup"><span data-stu-id="78b47-198">(8)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-199">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="78b47-199">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="78b47-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="78b47-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="78b47-201">(9)</span><span class="sxs-lookup"><span data-stu-id="78b47-201">(9)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-202">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-202">Device is not working properly.</span></span> <span data-ttu-id="78b47-203">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-203">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="78b47-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="78b47-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="78b47-205">(10)</span><span class="sxs-lookup"><span data-stu-id="78b47-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-206">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="78b47-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="78b47-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="78b47-208">(11)</span><span class="sxs-lookup"><span data-stu-id="78b47-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-209">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="78b47-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="78b47-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="78b47-211">12</span><span class="sxs-lookup"><span data-stu-id="78b47-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-212">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="78b47-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="78b47-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="78b47-214">(13)</span><span class="sxs-lookup"><span data-stu-id="78b47-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-215">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="78b47-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="78b47-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="78b47-217">(14)</span><span class="sxs-lookup"><span data-stu-id="78b47-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-218">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="78b47-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="78b47-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="78b47-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="78b47-220">(15)</span><span class="sxs-lookup"><span data-stu-id="78b47-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-221">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="78b47-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="78b47-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="78b47-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="78b47-223">(16)</span><span class="sxs-lookup"><span data-stu-id="78b47-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-224">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="78b47-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="78b47-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="78b47-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="78b47-226">(17)</span><span class="sxs-lookup"><span data-stu-id="78b47-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-227">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78b47-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78b47-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="78b47-229">(18)</span><span class="sxs-lookup"><span data-stu-id="78b47-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-230">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="78b47-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="78b47-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="78b47-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="78b47-232">(19)</span><span class="sxs-lookup"><span data-stu-id="78b47-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="78b47-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="78b47-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="78b47-234">(20)</span><span class="sxs-lookup"><span data-stu-id="78b47-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-235">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="78b47-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="78b47-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="78b47-237">(21)</span><span class="sxs-lookup"><span data-stu-id="78b47-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-238">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="78b47-238">System failure.</span></span> <span data-ttu-id="78b47-239">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="78b47-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="78b47-240">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="78b47-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="78b47-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="78b47-242">(22)</span><span class="sxs-lookup"><span data-stu-id="78b47-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-243">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="78b47-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="78b47-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="78b47-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="78b47-245">(23)</span><span class="sxs-lookup"><span data-stu-id="78b47-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-246">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="78b47-246">System failure.</span></span> <span data-ttu-id="78b47-247">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="78b47-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="78b47-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="78b47-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="78b47-249">(24)</span><span class="sxs-lookup"><span data-stu-id="78b47-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-250">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="78b47-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="78b47-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="78b47-252">(25)</span><span class="sxs-lookup"><span data-stu-id="78b47-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-253">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="78b47-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="78b47-255">(26)</span><span class="sxs-lookup"><span data-stu-id="78b47-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-256">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="78b47-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="78b47-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="78b47-258">(27)</span><span class="sxs-lookup"><span data-stu-id="78b47-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-259">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="78b47-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="78b47-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="78b47-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="78b47-261">(28)</span><span class="sxs-lookup"><span data-stu-id="78b47-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-262">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="78b47-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="78b47-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="78b47-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="78b47-264">(29)</span><span class="sxs-lookup"><span data-stu-id="78b47-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-265">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="78b47-265">Device is disabled.</span></span> <span data-ttu-id="78b47-266">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="78b47-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="78b47-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="78b47-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="78b47-268">(30)</span><span class="sxs-lookup"><span data-stu-id="78b47-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-269">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="78b47-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78b47-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="78b47-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="78b47-271">(31)</span><span class="sxs-lookup"><span data-stu-id="78b47-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-272">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-272">Device is not working properly.</span></span> <span data-ttu-id="78b47-273">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="78b47-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="78b47-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-275">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78b47-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-277">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="78b47-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-278">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="78b47-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="78b47-279">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-280">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="78b47-280">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-281">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78b47-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-283">Número de tempos limite do controlador SCSI que ocorreram desde a última redefinição.</span><span class="sxs-lookup"><span data-stu-id="78b47-283">Number of SCSI controller time-outs that have occurred since the last reset.</span></span>

</dd> <dt>

<span data-ttu-id="78b47-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78b47-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-287">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78b47-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78b47-288">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="78b47-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="78b47-289">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="78b47-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="78b47-290">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-291">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="78b47-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-294">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="78b47-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-295">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="78b47-295">Textual description of the object.</span></span>

<span data-ttu-id="78b47-296">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-297">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="78b47-297">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-300">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78b47-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78b47-301">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78b47-301">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="78b47-302">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-303">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="78b47-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-304">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78b47-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-306">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="78b47-306">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="78b47-307">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="78b47-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-311">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="78b47-311">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="78b47-312">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="78b47-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-314">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78b47-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-316">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="78b47-316">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-317">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="78b47-317">Date and time the object was installed.</span></span> <span data-ttu-id="78b47-318">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="78b47-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="78b47-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="78b47-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-321">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78b47-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-323">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78b47-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="78b47-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-325">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="78b47-325">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-326">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78b47-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-328">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="78b47-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-329">Largura máxima dos dados, em bits, com suporte do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="78b47-329">Maximum data width, in bits, supported by the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="78b47-330">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="78b47-330">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78b47-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="78b47-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-334">Número máximo de entidades diretamente endereçáveis com suporte pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="78b47-334">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="78b47-335">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="78b47-335">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="78b47-336">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-336">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-337">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="78b47-337">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-338">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="78b47-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-340">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="78b47-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-341">Taxa de transferência máxima, em bits por segundo, com suporte do controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="78b47-341">Maximum transfer rate, in bits-per-second, supported by the SCSI controller.</span></span>

<span data-ttu-id="78b47-342">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="78b47-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-343">**Nome**</span><span class="sxs-lookup"><span data-stu-id="78b47-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-346">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="78b47-346">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-347">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="78b47-347">Label by which the object is known.</span></span> <span data-ttu-id="78b47-348">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="78b47-348">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="78b47-349">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-350">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="78b47-350">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-353">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="78b47-353">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-354">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78b47-354">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="78b47-355">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="78b47-356">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="78b47-356">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="78b47-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="78b47-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-358">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78b47-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="78b47-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-360">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78b47-360">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="78b47-361">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="78b47-361">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78b47-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="78b47-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="78b47-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="78b47-363"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="78b47-364"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="78b47-364"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="78b47-365"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="78b47-365"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-366">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="78b47-366">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="78b47-367"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="78b47-367"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-368">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="78b47-368">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="78b47-369"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="78b47-369"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-370">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="78b47-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="78b47-371">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="78b47-371">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="78b47-372">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="78b47-372">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="78b47-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="78b47-373"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-374">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="78b47-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="78b47-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="78b47-375"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-376">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="78b47-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-377">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="78b47-377">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-378">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78b47-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-380">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="78b47-380">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="78b47-381">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="78b47-381">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="78b47-382">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="78b47-382">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="78b47-383">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="78b47-383">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="78b47-384">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-385">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="78b47-385">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-386">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78b47-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-388">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controlador de armazenamento DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="78b47-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-389">Indica se o controlador SCSI fornece redundância ou proteção contra falhas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78b47-389">Indicates whether the SCSI controller provides redundancy or protection against device failures.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78b47-390"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78b47-390"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78b47-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78b47-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="78b47-392"><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>**Desprotegido** (3)</span><span class="sxs-lookup"><span data-stu-id="78b47-392"><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="78b47-393"><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>**Protegido** (4)</span><span class="sxs-lookup"><span data-stu-id="78b47-393"><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="78b47-394"><span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>**Protegido por meio do SCC (comando do controlador SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="78b47-394"><span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-395">Protegido por SCC (comando do controlador SCSI-3)</span><span class="sxs-lookup"><span data-stu-id="78b47-395">Protected by SCC (SCSI-3 controller command)</span></span>

</dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="78b47-396"><span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>**Protegido por meio do SCC-2 (comando do controlador SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="78b47-396"><span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="78b47-397">Protegido por SCC-2 (comando do controlador SCSI-3)</span><span class="sxs-lookup"><span data-stu-id="78b47-397">Protected by SCC-2 (SCSI-3 controller command)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-398">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="78b47-398">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-399">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78b47-399">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-401">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="78b47-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-402">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="78b47-402">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="78b47-403">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="78b47-404">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="78b47-404">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78b47-405">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78b47-405">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78b47-406">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78b47-406">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="78b47-407">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="78b47-407">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="78b47-408">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="78b47-408">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="78b47-409">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="78b47-409">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="78b47-410">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="78b47-410">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="78b47-411">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="78b47-411">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="78b47-412">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="78b47-412">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="78b47-413">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="78b47-413">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="78b47-414">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="78b47-414">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="78b47-415">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="78b47-415">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="78b47-416">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="78b47-416">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="78b47-417">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="78b47-417">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="78b47-418">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="78b47-418">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="78b47-419">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="78b47-419">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="78b47-420">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="78b47-420">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="78b47-421">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="78b47-421">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="78b47-422">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="78b47-422">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="78b47-423">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="78b47-423">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="78b47-424">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="78b47-424">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="78b47-425">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="78b47-425">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="78b47-426">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="78b47-426">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="78b47-427">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="78b47-427">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="78b47-428">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="78b47-428">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="78b47-429">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="78b47-429">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="78b47-430">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="78b47-430">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="78b47-431">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="78b47-431">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="78b47-432">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="78b47-432">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="78b47-433">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="78b47-433">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="78b47-434">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="78b47-434">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="78b47-435">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="78b47-435">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="78b47-436">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="78b47-436">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="78b47-437">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="78b47-437">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="78b47-438">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="78b47-438">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="78b47-439">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="78b47-439">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="78b47-440">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="78b47-440">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="78b47-441">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="78b47-441">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="78b47-442">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="78b47-442">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="78b47-443">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="78b47-443">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="78b47-444">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="78b47-444">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="78b47-445">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="78b47-445">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="78b47-446">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="78b47-446">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="78b47-447">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="78b47-447">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="78b47-448">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="78b47-448">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="78b47-449">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="78b47-449">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="78b47-450">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="78b47-450">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="78b47-451">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="78b47-451">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-452">**Status**</span><span class="sxs-lookup"><span data-stu-id="78b47-452">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-453">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-455">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="78b47-455">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-456">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="78b47-456">Current status of the object.</span></span> <span data-ttu-id="78b47-457">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="78b47-458">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="78b47-458">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="78b47-459">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="78b47-459">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="78b47-460">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="78b47-460">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78b47-461">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="78b47-461">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78b47-462">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="78b47-462">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="78b47-463">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="78b47-463">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="78b47-464">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="78b47-464">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="78b47-465">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="78b47-465">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="78b47-466">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="78b47-466">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="78b47-467">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="78b47-467">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="78b47-468">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="78b47-468">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="78b47-469">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="78b47-469">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="78b47-470">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="78b47-470">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-471">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="78b47-471">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-472">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78b47-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-474">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="78b47-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="78b47-475">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="78b47-475">State of the logical device.</span></span> <span data-ttu-id="78b47-476">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="78b47-476">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="78b47-477">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78b47-478">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="78b47-478">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78b47-479">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78b47-479">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="78b47-480">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="78b47-480">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="78b47-481">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="78b47-481">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="78b47-482">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="78b47-482">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78b47-483">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78b47-483">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-485">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-486">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78b47-486">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78b47-487">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="78b47-487">Scoping system's creation class name.</span></span>

<span data-ttu-id="78b47-488">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-488">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-489">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="78b47-489">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-490">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78b47-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-491">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78b47-492">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78b47-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78b47-493">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="78b47-493">Scoping system's name.</span></span>

<span data-ttu-id="78b47-494">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b47-495">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="78b47-495">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78b47-496">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78b47-496">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78b47-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78b47-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78b47-498">Data e hora da última redefinição do controlador, o que significa que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="78b47-498">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="78b47-499">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-499">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78b47-500">Comentários</span><span class="sxs-lookup"><span data-stu-id="78b47-500">Remarks</span></span>

<span data-ttu-id="78b47-501">A classe **CIM \_ SCSIController** é derivada do [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-501">The **CIM\_SCSIController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="78b47-502">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="78b47-502">WMI does not implement this class.</span></span> <span data-ttu-id="78b47-503">Para classes WMI derivadas do **CIM \_ SCSIController**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="78b47-503">For WMI classes derived from **CIM\_SCSIController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="78b47-504">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="78b47-504">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="78b47-505">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="78b47-505">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="78b47-506">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78b47-506">Requirements</span></span>



| <span data-ttu-id="78b47-507">Requisito</span><span class="sxs-lookup"><span data-stu-id="78b47-507">Requirement</span></span> | <span data-ttu-id="78b47-508">Valor</span><span class="sxs-lookup"><span data-stu-id="78b47-508">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78b47-509">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78b47-509">Minimum supported client</span></span><br/> | <span data-ttu-id="78b47-510">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78b47-510">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78b47-511">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78b47-511">Minimum supported server</span></span><br/> | <span data-ttu-id="78b47-512">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78b47-512">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78b47-513">Namespace</span><span class="sxs-lookup"><span data-stu-id="78b47-513">Namespace</span></span><br/>                | <span data-ttu-id="78b47-514">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="78b47-514">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78b47-515">MOF</span><span class="sxs-lookup"><span data-stu-id="78b47-515">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78b47-516"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78b47-516"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78b47-517">DLL</span><span class="sxs-lookup"><span data-stu-id="78b47-517">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78b47-518"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78b47-518"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b47-519">Confira também</span><span class="sxs-lookup"><span data-stu-id="78b47-519">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b47-520">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="78b47-520">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

