---
description: A \_ classe CIM DiskDrive representa uma unidade de disco físico, como visto pelo sistema operacional.
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: Classe CIM_DiskDrive (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164105"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="a079c-103">Classe CIM_DiskDrive (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a079c-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a079c-104">A classe **CIM \_ DiskDrive** representa uma unidade de disco físico, como visto pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a079c-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="a079c-105">Os recursos da unidade de disco correspondem às características lógica e de gerenciamento da unidade e, em alguns casos, podem não refletir as características físicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="a079c-106">Uma interface para uma unidade física é um membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a079c-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="a079c-107">No entanto, um objeto baseado em outro dispositivo lógico não é membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a079c-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a079c-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a079c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a079c-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a079c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a079c-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a079c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a079c-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a079c-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a079c-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a079c-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a079c-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a079c-113">Members</span></span>

<span data-ttu-id="a079c-114">A classe **CIM \_ DiskDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a079c-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="a079c-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="a079c-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="a079c-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a079c-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a079c-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="a079c-117">Methods</span></span>

<span data-ttu-id="a079c-118">A classe **CIM \_ DiskDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a079c-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="a079c-119">Método</span><span class="sxs-lookup"><span data-stu-id="a079c-119">Method</span></span>                                                                | <span data-ttu-id="a079c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a079c-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a079c-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a079c-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="a079c-122">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="a079c-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="a079c-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a079c-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a079c-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="a079c-125">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="a079c-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a079c-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="a079c-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a079c-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a079c-127">Properties</span></span>

<span data-ttu-id="a079c-128">A classe **CIM \_ DiskDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a079c-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a079c-129">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="a079c-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a079c-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a079c-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-133">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-133">Availability and status of the device.</span></span>

<span data-ttu-id="a079c-134">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a079c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a079c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-136">Outros.</span><span class="sxs-lookup"><span data-stu-id="a079c-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a079c-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a079c-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-138">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a079c-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a079c-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a079c-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-140">Execução/energia completa.</span><span class="sxs-lookup"><span data-stu-id="a079c-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a079c-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a079c-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-142">Aviso.</span><span class="sxs-lookup"><span data-stu-id="a079c-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a079c-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="a079c-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-144">Testes.</span><span class="sxs-lookup"><span data-stu-id="a079c-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a079c-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="a079c-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-146">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="a079c-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a079c-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="a079c-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-148">Desligar.</span><span class="sxs-lookup"><span data-stu-id="a079c-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a079c-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="a079c-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="a079c-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a079c-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="a079c-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-152">Fora de serviço.</span><span class="sxs-lookup"><span data-stu-id="a079c-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a079c-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a079c-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-154">Degradado.</span><span class="sxs-lookup"><span data-stu-id="a079c-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a079c-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a079c-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-156">Não instalado.</span><span class="sxs-lookup"><span data-stu-id="a079c-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a079c-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="a079c-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-158">Erro de instalação.</span><span class="sxs-lookup"><span data-stu-id="a079c-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a079c-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="a079c-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-160">É conhecido que o dispositivo esteja em um modo de economia de energia, mas seu status exato nesse modo é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a079c-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a079c-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="a079c-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-162">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="a079c-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a079c-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a079c-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-164">O dispositivo não está funcionando, mas pode ser levado a energia completa ' rapidamente '.</span><span class="sxs-lookup"><span data-stu-id="a079c-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a079c-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="a079c-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-166">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="a079c-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a079c-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a079c-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-168">O dispositivo está em um estado de aviso e também em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="a079c-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a079c-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a079c-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-170">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="a079c-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a079c-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a079c-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-172">Não está pronto.</span><span class="sxs-lookup"><span data-stu-id="a079c-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a079c-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a079c-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-174">Não configurado.</span><span class="sxs-lookup"><span data-stu-id="a079c-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a079c-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="a079c-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-176">A unidade de disco não está disponível.</span><span class="sxs-lookup"><span data-stu-id="a079c-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-177">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="a079c-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-178">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a079c-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a079c-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-180">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="a079c-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-181">Recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="a079c-181">Capabilities of the media access device.</span></span> <span data-ttu-id="a079c-182">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a079c-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a079c-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-184">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a079c-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a079c-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a079c-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-186">Outros.</span><span class="sxs-lookup"><span data-stu-id="a079c-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="a079c-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="a079c-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-188">Acesso sequencial.</span><span class="sxs-lookup"><span data-stu-id="a079c-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="a079c-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="a079c-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-190">Acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="a079c-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="a079c-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="a079c-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-192">Criando.</span><span class="sxs-lookup"><span data-stu-id="a079c-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="a079c-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="a079c-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-194">Criptografia.</span><span class="sxs-lookup"><span data-stu-id="a079c-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="a079c-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="a079c-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-196">Compactação.</span><span class="sxs-lookup"><span data-stu-id="a079c-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="a079c-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="a079c-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-198">Mídia removível.</span><span class="sxs-lookup"><span data-stu-id="a079c-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="a079c-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="a079c-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-200">Limpeza manual.</span><span class="sxs-lookup"><span data-stu-id="a079c-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="a079c-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="a079c-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-202">Limpeza automática.</span><span class="sxs-lookup"><span data-stu-id="a079c-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="a079c-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="a079c-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-204">Notificação inteligente.</span><span class="sxs-lookup"><span data-stu-id="a079c-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="a079c-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="a079c-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-206">Distingue um dispositivo que pode acessar ambos os lados da mídia de dois lados de um dispositivo que lê apenas um único lado e requer que a mídia seja transferida.</span><span class="sxs-lookup"><span data-stu-id="a079c-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="a079c-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="a079c-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-208">Indica que a mídia não precisa ser desejetada explicitamente do dispositivo antes de ser acessada por um elemento de seletor.</span><span class="sxs-lookup"><span data-stu-id="a079c-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-209">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a079c-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-210">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a079c-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-212">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="a079c-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-213">Matriz de cadeias de caracteres de forma livre que fornecem explicações detalhadas para acessar recursos do dispositivo indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="a079c-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="a079c-214">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="a079c-215">Cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="a079c-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="a079c-216">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a079c-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-219">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a079c-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-220">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a079c-220">Short textual description of the object.</span></span>

<span data-ttu-id="a079c-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-222">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="a079c-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-225">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="a079c-226">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="a079c-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="a079c-227">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="a079c-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="a079c-228">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="a079c-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="a079c-229">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="a079c-230">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a079c-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="a079c-231">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="a079c-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="a079c-232">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="a079c-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="a079c-233">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="a079c-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="a079c-234">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="a079c-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="a079c-235">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="a079c-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-236">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a079c-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-237">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a079c-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-239">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a079c-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-240">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a079c-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="a079c-241">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a079c-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a079c-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a079c-243"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="a079c-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-244">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a079c-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a079c-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a079c-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a079c-246">(1)</span><span class="sxs-lookup"><span data-stu-id="a079c-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-247">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a079c-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a079c-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a079c-249">(2)</span><span class="sxs-lookup"><span data-stu-id="a079c-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a079c-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a079c-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a079c-251">(3)</span><span class="sxs-lookup"><span data-stu-id="a079c-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-252">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="a079c-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a079c-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a079c-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a079c-254">(4)</span><span class="sxs-lookup"><span data-stu-id="a079c-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-255">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a079c-255">Device is not working properly.</span></span> <span data-ttu-id="a079c-256">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a079c-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a079c-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="a079c-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a079c-258">(5)</span><span class="sxs-lookup"><span data-stu-id="a079c-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-259">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="a079c-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a079c-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a079c-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a079c-261"> (6)</span><span class="sxs-lookup"><span data-stu-id="a079c-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-262">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a079c-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a079c-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a079c-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a079c-264">(7)</span><span class="sxs-lookup"><span data-stu-id="a079c-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a079c-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="a079c-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a079c-266">(8)</span><span class="sxs-lookup"><span data-stu-id="a079c-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-267">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="a079c-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a079c-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="a079c-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a079c-269">(9)</span><span class="sxs-lookup"><span data-stu-id="a079c-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-270">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a079c-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="a079c-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a079c-272">(10)</span><span class="sxs-lookup"><span data-stu-id="a079c-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-273">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a079c-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="a079c-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a079c-275">(11)</span><span class="sxs-lookup"><span data-stu-id="a079c-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-276">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a079c-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="a079c-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a079c-278">12</span><span class="sxs-lookup"><span data-stu-id="a079c-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-279">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="a079c-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a079c-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a079c-281">(13)</span><span class="sxs-lookup"><span data-stu-id="a079c-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-282">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a079c-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="a079c-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a079c-284">(14)</span><span class="sxs-lookup"><span data-stu-id="a079c-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-285">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a079c-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a079c-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="a079c-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a079c-287">(15)</span><span class="sxs-lookup"><span data-stu-id="a079c-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-288">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="a079c-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a079c-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="a079c-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a079c-290">(16)</span><span class="sxs-lookup"><span data-stu-id="a079c-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-291">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="a079c-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a079c-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="a079c-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a079c-293">(17)</span><span class="sxs-lookup"><span data-stu-id="a079c-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-294">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a079c-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a079c-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a079c-296">(18)</span><span class="sxs-lookup"><span data-stu-id="a079c-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-297">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="a079c-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a079c-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="a079c-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a079c-299">(19)</span><span class="sxs-lookup"><span data-stu-id="a079c-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a079c-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a079c-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a079c-301">(20)</span><span class="sxs-lookup"><span data-stu-id="a079c-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-302">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a079c-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a079c-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a079c-304">(21)</span><span class="sxs-lookup"><span data-stu-id="a079c-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-305">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a079c-305">System failure.</span></span> <span data-ttu-id="a079c-306">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a079c-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a079c-307">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a079c-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a079c-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a079c-309">(22)</span><span class="sxs-lookup"><span data-stu-id="a079c-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-310">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a079c-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a079c-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="a079c-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a079c-312">(23)</span><span class="sxs-lookup"><span data-stu-id="a079c-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-313">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a079c-313">System failure.</span></span> <span data-ttu-id="a079c-314">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a079c-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a079c-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="a079c-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a079c-316">(24)</span><span class="sxs-lookup"><span data-stu-id="a079c-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-317">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="a079c-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a079c-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a079c-319">(25)</span><span class="sxs-lookup"><span data-stu-id="a079c-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-320">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a079c-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a079c-322">(26)</span><span class="sxs-lookup"><span data-stu-id="a079c-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-323">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a079c-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="a079c-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a079c-325">(27)</span><span class="sxs-lookup"><span data-stu-id="a079c-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-326">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="a079c-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a079c-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="a079c-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a079c-328">(28)</span><span class="sxs-lookup"><span data-stu-id="a079c-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-329">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="a079c-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a079c-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="a079c-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a079c-331">(29)</span><span class="sxs-lookup"><span data-stu-id="a079c-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-332">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="a079c-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a079c-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a079c-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a079c-334">(30)</span><span class="sxs-lookup"><span data-stu-id="a079c-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-335">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a079c-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a079c-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a079c-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a079c-337">(31)</span><span class="sxs-lookup"><span data-stu-id="a079c-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-338">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="a079c-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-339">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a079c-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-340">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a079c-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-342">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a079c-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-343">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a079c-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a079c-344">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-345">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a079c-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-348">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a079c-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a079c-349">Nome da classe (ou subclasse) usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a079c-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="a079c-350">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a079c-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a079c-351">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-352">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="a079c-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-353">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a079c-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-355">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a079c-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-356">Tamanho de bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="a079c-357">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a079c-358">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a079c-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-359">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a079c-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-362">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a079c-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-363">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a079c-363">Textual description of the object.</span></span>

<span data-ttu-id="a079c-364">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-365">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a079c-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-366">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-368">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a079c-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a079c-369">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a079c-370">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-371">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a079c-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-372">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a079c-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-374">Se **for true**, o erro relatado na propriedade **LastErrorCode** será limpo.</span><span class="sxs-lookup"><span data-stu-id="a079c-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="a079c-375">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a079c-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-377">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-379">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="a079c-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a079c-380">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-381">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="a079c-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-384">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="a079c-385">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a079c-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-387">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a079c-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-389">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a079c-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-390">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a079c-390">Date and time when the object was installed.</span></span> <span data-ttu-id="a079c-391">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a079c-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a079c-392">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a079c-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-394">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a079c-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-396">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a079c-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-398">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="a079c-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-399">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a079c-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-401">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a079c-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-402">Tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="a079c-403">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a079c-404">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a079c-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-405">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="a079c-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-406">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a079c-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-408">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="a079c-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-409">Tamanho máximo, em quilobytes, de mídia com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="a079c-410">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="a079c-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="a079c-411">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a079c-412">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a079c-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-413">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="a079c-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-414">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a079c-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-416">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a079c-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-417">Tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a079c-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="a079c-418">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a079c-419">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a079c-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-420">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a079c-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-423">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a079c-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-424">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a079c-424">Label by which the object is known.</span></span> <span data-ttu-id="a079c-425">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="a079c-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a079c-426">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-427">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="a079c-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-428">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a079c-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-430">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="a079c-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="a079c-431">A limpeza manual ou automática é possível é indicada na propriedade da matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="a079c-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="a079c-432">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-433">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="a079c-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-434">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a079c-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-436">Quando o dispositivo de acesso à mídia dá suporte a várias mídias individuais, essa propriedade define o número máximo que pode ser suportado ou inserido.</span><span class="sxs-lookup"><span data-stu-id="a079c-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="a079c-437">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a079c-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-441">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a079c-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-442">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a079c-443">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a079c-444">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a079c-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a079c-445">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a079c-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-446">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a079c-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a079c-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-448">Recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="a079c-449">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a079c-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a079c-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-451">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a079c-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a079c-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="a079c-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-453">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="a079c-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a079c-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a079c-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-455">Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a079c-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a079c-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a079c-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-457">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a079c-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a079c-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a079c-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-459">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="a079c-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a079c-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="a079c-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-461">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="a079c-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a079c-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="a079c-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-463">O método [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="a079c-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a079c-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="a079c-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a079c-465">O método [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="a079c-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-466">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a079c-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-467">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a079c-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a079c-469">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="a079c-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a079c-470">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a079c-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a079c-471">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="a079c-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a079c-472">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a079c-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="a079c-473">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-474">**Status**</span><span class="sxs-lookup"><span data-stu-id="a079c-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-477">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a079c-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-478">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a079c-478">Current status of the object.</span></span>

<span data-ttu-id="a079c-479">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a079c-480">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a079c-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a079c-481">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a079c-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a079c-482">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a079c-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a079c-483">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a079c-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a079c-484">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a079c-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a079c-485">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a079c-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a079c-486">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a079c-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a079c-487">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a079c-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a079c-488">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a079c-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a079c-489">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a079c-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a079c-490">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a079c-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a079c-491">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a079c-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a079c-492">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a079c-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a079c-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-494">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a079c-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-496">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="a079c-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a079c-497">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a079c-497">State of the logical device.</span></span> <span data-ttu-id="a079c-498">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="a079c-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a079c-499">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a079c-500">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a079c-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a079c-501">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a079c-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a079c-502">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a079c-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a079c-503">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a079c-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a079c-504">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="a079c-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a079c-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a079c-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-506">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-508">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a079c-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a079c-509">Propriedade **CreationClassName** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a079c-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="a079c-510">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a079c-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a079c-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a079c-512">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a079c-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a079c-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a079c-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a079c-514">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a079c-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a079c-515">Propriedade de **nome** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a079c-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="a079c-516">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a079c-517">Comentários</span><span class="sxs-lookup"><span data-stu-id="a079c-517">Remarks</span></span>

<span data-ttu-id="a079c-518">A classe **CIM \_ DiskDrive** é derivada de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a079c-519">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a079c-519">WMI does not implement this class.</span></span> <span data-ttu-id="a079c-520">Consulte [classes Win32](win32-provider.md) para classes derivadas do **CIM \_ DiskDrive**.</span><span class="sxs-lookup"><span data-stu-id="a079c-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="a079c-521">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a079c-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a079c-522">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a079c-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a079c-523">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a079c-523">Requirements</span></span>



| <span data-ttu-id="a079c-524">Requisito</span><span class="sxs-lookup"><span data-stu-id="a079c-524">Requirement</span></span> | <span data-ttu-id="a079c-525">Valor</span><span class="sxs-lookup"><span data-stu-id="a079c-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a079c-526">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a079c-526">Minimum supported client</span></span><br/> | <span data-ttu-id="a079c-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a079c-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a079c-528">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a079c-528">Minimum supported server</span></span><br/> | <span data-ttu-id="a079c-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a079c-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a079c-530">Namespace</span><span class="sxs-lookup"><span data-stu-id="a079c-530">Namespace</span></span><br/>                | <span data-ttu-id="a079c-531">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a079c-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a079c-532">MOF</span><span class="sxs-lookup"><span data-stu-id="a079c-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a079c-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a079c-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a079c-534">DLL</span><span class="sxs-lookup"><span data-stu-id="a079c-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a079c-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a079c-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a079c-536">Confira também</span><span class="sxs-lookup"><span data-stu-id="a079c-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a079c-537">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a079c-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

