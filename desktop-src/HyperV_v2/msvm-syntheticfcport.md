---
description: Representa uma porta de Fibre Channel sintética.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Classe Msvm_SyntheticFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090010"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="fbb90-103">\_Classe Msvm SyntheticFcPort</span><span class="sxs-lookup"><span data-stu-id="fbb90-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="fbb90-104">Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="fbb90-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="fbb90-105">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="fbb90-106">Representa uma porta de Fibre Channel sintética.</span><span class="sxs-lookup"><span data-stu-id="fbb90-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="fbb90-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fbb90-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb90-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbb90-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="fbb90-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fbb90-109">Members</span></span>

<span data-ttu-id="fbb90-110">A classe **Msvm \_ SyntheticFcPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fbb90-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="fbb90-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fbb90-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fbb90-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fbb90-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fbb90-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fbb90-113">Methods</span></span>

<span data-ttu-id="fbb90-114">A classe **Msvm \_ SyntheticFcPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fbb90-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="fbb90-115">Método</span><span class="sxs-lookup"><span data-stu-id="fbb90-115">Method</span></span>                                                                | <span data-ttu-id="fbb90-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbb90-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="fbb90-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="fbb90-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="fbb90-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fbb90-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbb90-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="fbb90-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="fbb90-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fbb90-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbb90-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="fbb90-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="fbb90-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fbb90-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="fbb90-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="fbb90-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="fbb90-124">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="fbb90-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="fbb90-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="fbb90-126">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="fbb90-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="fbb90-127">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="fbb90-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="fbb90-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fbb90-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbb90-129">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="fbb90-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="fbb90-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fbb90-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbb90-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fbb90-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="fbb90-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fbb90-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fbb90-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fbb90-133">Properties</span></span>

<span data-ttu-id="fbb90-134">A classe **Msvm \_ SyntheticFcPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fbb90-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="fbb90-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-136">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-138">Uma matriz de inteiros que indica as classes de serviço que estão ativas.</span><span class="sxs-lookup"><span data-stu-id="fbb90-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="fbb90-139">O COS com suporte é especificado pela propriedade **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="fbb90-140">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="fbb90-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="fbb90-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="fbb90-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="fbb90-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-150">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-152">Uma matriz de inteiros que indica o Fibre Channel protocolos FC-4 em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="fbb90-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="fbb90-153">Uma lista de todos os protocolos com suporte é especificada pela propriedade **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="fbb90-154">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sobre FC** (5)</span><span class="sxs-lookup"><span data-stu-id="fbb90-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="fbb90-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="fbb90-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 mestre** (17)</span><span class="sxs-lookup"><span data-stu-id="fbb90-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 escravo** (18)</span><span class="sxs-lookup"><span data-stu-id="fbb90-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 par** (19)</span><span class="sxs-lookup"><span data-stu-id="fbb90-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="fbb90-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 escravo** (22)</span><span class="sxs-lookup"><span data-stu-id="fbb90-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 par** (23)</span><span class="sxs-lookup"><span data-stu-id="fbb90-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="fbb90-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidade de controle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="fbb90-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="fbb90-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidade de controle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="fbb90-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="fbb90-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="fbb90-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="fbb90-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="fbb90-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controle bbl** (80)</span><span class="sxs-lookup"><span data-stu-id="fbb90-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada bbl FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="fbb90-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="fbb90-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="fbb90-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="fbb90-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Exclusivo do fornecedor** (255)</span><span class="sxs-lookup"><span data-stu-id="fbb90-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="fbb90-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-182">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-184">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fbb90-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-185">A unidade de transmissão máxima (MTU) do negociada ou ativa que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fbb90-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="fbb90-186">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="fbb90-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-188">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-190">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="fbb90-191">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-192">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="fbb90-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-193">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fbb90-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-195">Indica se a porta é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="fbb90-196">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-197">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="fbb90-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-200">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-200">The primary availability and status of the device.</span></span> <span data-ttu-id="fbb90-201">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="fbb90-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-203">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-205">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="fbb90-206">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-207">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="fbb90-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-210">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb90-210">A short description of the object.</span></span> <span data-ttu-id="fbb90-211">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="fbb90-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-215">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="fbb90-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="fbb90-216">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbb90-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbb90-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fbb90-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbb90-225">)</span><span class="sxs-lookup"><span data-stu-id="fbb90-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fbb90-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-229">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-229">The scoping system's creation class name.</span></span> <span data-ttu-id="fbb90-230">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbb90-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-231">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbb90-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-234">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="fbb90-234">A description of the object.</span></span> <span data-ttu-id="fbb90-235">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="fbb90-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-239">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="fbb90-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="fbb90-240">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbb90-241">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="fbb90-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbb90-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fbb90-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbb90-250">)</span><span class="sxs-lookup"><span data-stu-id="fbb90-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="fbb90-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-254">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbb90-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="fbb90-255">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbb90-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fbb90-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-259">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb90-259">A display name for the object.</span></span> <span data-ttu-id="fbb90-260">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="fbb90-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-262">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-264">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="fbb90-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="fbb90-265">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="fbb90-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fbb90-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-269">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="fbb90-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="fbb90-270">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fbb90-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="fbb90-271">Valor</span><span class="sxs-lookup"><span data-stu-id="fbb90-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="fbb90-272">Significado</span><span class="sxs-lookup"><span data-stu-id="fbb90-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fbb90-273"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="fbb90-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="fbb90-274">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="fbb90-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="fbb90-275"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="fbb90-276"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="fbb90-277">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="fbb90-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fbb90-278"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="fbb90-279">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="fbb90-280"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="fbb90-281">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="fbb90-282"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="fbb90-283">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="fbb90-284"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="fbb90-285">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="fbb90-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="fbb90-286"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="fbb90-287">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="fbb90-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="fbb90-288"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="fbb90-289">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="fbb90-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="fbb90-290"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="fbb90-291">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="fbb90-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="fbb90-292">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="fbb90-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="fbb90-293">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="fbb90-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="fbb90-294"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="fbb90-295">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="fbb90-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="fbb90-296">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="fbb90-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="fbb90-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fbb90-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-298">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fbb90-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-300">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="fbb90-301">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fbb90-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-305">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="fbb90-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="fbb90-306">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="fbb90-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-308">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fbb90-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-310">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="fbb90-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="fbb90-311">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="fbb90-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-313">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-315">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="fbb90-315">The current health of the element.</span></span> <span data-ttu-id="fbb90-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fbb90-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-318">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-320">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="fbb90-321">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fbb90-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-323">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fbb90-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-325">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-325">The date and time when the object was installed.</span></span> <span data-ttu-id="fbb90-326">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="fbb90-327">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fbb90-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-331">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="fbb90-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-332">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="fbb90-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fbb90-333">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fbb90-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbb90-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-337">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbb90-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="fbb90-338">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="fbb90-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-340">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-342">Especifica o tipo de tecnologia de link para a porta.</span><span class="sxs-lookup"><span data-stu-id="fbb90-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="fbb90-343">Quando definido como 1 (outro), a propriedade **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="fbb90-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="fbb90-344">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="fbb90-345">Valor</span><span class="sxs-lookup"><span data-stu-id="fbb90-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="fbb90-346">Significado</span><span class="sxs-lookup"><span data-stu-id="fbb90-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="fbb90-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="fbb90-348">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="fbb90-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fbb90-349">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="fbb90-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-350">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-352">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="fbb90-352">This property has been deprecated.</span></span> <span data-ttu-id="fbb90-353">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-354">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="fbb90-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-355">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-357">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fbb90-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-358">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="fbb90-359">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbb90-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-360">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fbb90-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-363">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="fbb90-363">The label by which the object is known.</span></span> <span data-ttu-id="fbb90-364">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-365">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="fbb90-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-366">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-368">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="fbb90-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-369">Uma matriz de cadeias de caracteres que contêm os endereços MAC para a porta.</span><span class="sxs-lookup"><span data-stu-id="fbb90-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="fbb90-370">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-371">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="fbb90-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-372">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-374">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="fbb90-375">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbb90-376">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="fbb90-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="fbb90-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="fbb90-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="fbb90-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="fbb90-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="fbb90-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="fbb90-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="fbb90-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="fbb90-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="fbb90-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="fbb90-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="fbb90-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbb90-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fbb90-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbb90-396">)</span><span class="sxs-lookup"><span data-stu-id="fbb90-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="fbb90-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-398">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-400">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb90-400">The current statuses of the object.</span></span> <span data-ttu-id="fbb90-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-402">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="fbb90-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-405">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="fbb90-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="fbb90-406">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="fbb90-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="fbb90-407">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="fbb90-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-409">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-411">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbb90-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="fbb90-412">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-413">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="fbb90-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-414">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-416">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1, (outro).</span><span class="sxs-lookup"><span data-stu-id="fbb90-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="fbb90-417">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-418">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="fbb90-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-419">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-421">O uso dessa propriedade é preterido no lugar da propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="fbb90-422">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-423">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="fbb90-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-426">Descreve o tipo de módulo, quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="fbb90-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="fbb90-427">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbb90-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-428">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="fbb90-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-429">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-431">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="fbb90-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-432">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="fbb90-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="fbb90-433">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="fbb90-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="fbb90-434">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="fbb90-435">Essa propriedade deverá ser **nula** se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="fbb90-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="fbb90-436">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-437">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="fbb90-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-438">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-440">O número da porta.</span><span class="sxs-lookup"><span data-stu-id="fbb90-440">The port number.</span></span> <span data-ttu-id="fbb90-441">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-442">**PortType**</span><span class="sxs-lookup"><span data-stu-id="fbb90-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-443">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-445">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="fbb90-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="fbb90-446">Quando definido como 1 (outro), a propriedade **OtherPortType** relacionada contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="fbb90-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="fbb90-447">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbb90-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>+ **/50 10BaseT de cobre** (50)</span><span class="sxs-lookup"><span data-stu-id="fbb90-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="fbb90-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="fbb90-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="fbb90-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="fbb90-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="fbb90-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="fbb90-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="fbb90-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="fbb90-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="fbb90-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="fbb90-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="fbb90-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="fbb90-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="fbb90-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="fbb90-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="fbb90-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="fbb90-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="fbb90-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="fbb90-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fbb90-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-470">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fbb90-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-471">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-473">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-473">The power management capabilities of the device.</span></span> <span data-ttu-id="fbb90-474">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-475">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fbb90-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-476">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fbb90-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-478">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="fbb90-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="fbb90-479">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-480">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="fbb90-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-481">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-483">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="fbb90-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="fbb90-484">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-485">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="fbb90-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-486">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-488">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="fbb90-488">Provides high level status information.</span></span> <span data-ttu-id="fbb90-489">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="fbb90-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="fbb90-490">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbb90-491">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbb90-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fbb90-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbb90-498">)</span><span class="sxs-lookup"><span data-stu-id="fbb90-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-499">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="fbb90-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-500">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-501">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="fbb90-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-502">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fbb90-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-503">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="fbb90-504">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="fbb90-505">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbb90-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="fbb90-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-507">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-508">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-509">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="fbb90-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="fbb90-510">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="fbb90-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-511">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="fbb90-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-512">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-514">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fbb90-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-515">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="fbb90-516">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbb90-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-517">**Status**</span><span class="sxs-lookup"><span data-stu-id="fbb90-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-518">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-520">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="fbb90-520">The current status of the object.</span></span> <span data-ttu-id="fbb90-521">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-522">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fbb90-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-523">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-525">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="fbb90-526">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbb90-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fbb90-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-528">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-529">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-530">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbb90-530">The current state of the logical device.</span></span> <span data-ttu-id="fbb90-531">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-532">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="fbb90-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-533">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-534">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-535">Uma matriz de inteiros que indica o Fibre Channel classes de serviço (COS) que têm suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb90-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="fbb90-536">O COS ativo é especificado pela propriedade **ActiveCOS** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="fbb90-537">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-539"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-540"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-541"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-542"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-543"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="fbb90-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-544"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="fbb90-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-545"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="fbb90-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="fbb90-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-547">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-549">Uma matriz de inteiros que indica o Fibre Channel protocolos FC-4 com suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb90-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="fbb90-550">Os protocolos que estão ativos e em execução são especificados pela propriedade **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="fbb90-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="fbb90-551">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fbb90-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sobre FC** (5)</span><span class="sxs-lookup"><span data-stu-id="fbb90-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="fbb90-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="fbb90-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 mestre** (17)</span><span class="sxs-lookup"><span data-stu-id="fbb90-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 escravo** (18)</span><span class="sxs-lookup"><span data-stu-id="fbb90-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 par** (19)</span><span class="sxs-lookup"><span data-stu-id="fbb90-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="fbb90-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 escravo** (22)</span><span class="sxs-lookup"><span data-stu-id="fbb90-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 par** (23)</span><span class="sxs-lookup"><span data-stu-id="fbb90-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="fbb90-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidade de controle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="fbb90-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="fbb90-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidade de controle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="fbb90-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="fbb90-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="fbb90-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="fbb90-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="fbb90-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controle bbl** (80)</span><span class="sxs-lookup"><span data-stu-id="fbb90-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada bbl FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="fbb90-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="fbb90-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="fbb90-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="fbb90-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Exclusivo do fornecedor** (255)</span><span class="sxs-lookup"><span data-stu-id="fbb90-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbb90-578">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="fbb90-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-579">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-580">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-581">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fbb90-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-582">A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fbb90-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="fbb90-583">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbb90-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-584">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fbb90-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-585">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-586">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-587">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-587">The scoping system's creation class name.</span></span> <span data-ttu-id="fbb90-588">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbb90-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fbb90-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-590">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fbb90-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-591">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-592">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="fbb90-592">The scoping system's name.</span></span> <span data-ttu-id="fbb90-593">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbb90-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-594">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="fbb90-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-595">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fbb90-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-596">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-597">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="fbb90-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="fbb90-598">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-599">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="fbb90-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-600">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbb90-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-601">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-602">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="fbb90-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="fbb90-603">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fbb90-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-604">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="fbb90-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-605">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-606">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-607">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="fbb90-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="fbb90-608">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fbb90-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbb90-609">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="fbb90-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbb90-610">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbb90-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-611">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fbb90-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbb90-612">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="fbb90-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="fbb90-613">Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts.</span><span class="sxs-lookup"><span data-stu-id="fbb90-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="fbb90-614">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="fbb90-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="fbb90-615">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbb90-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fbb90-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbb90-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Somente front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="fbb90-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Somente back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="fbb90-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbb90-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Não restrito** (4)</span><span class="sxs-lookup"><span data-stu-id="fbb90-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbb90-620">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbb90-620">Requirements</span></span>



| <span data-ttu-id="fbb90-621">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbb90-621">Requirement</span></span> | <span data-ttu-id="fbb90-622">Valor</span><span class="sxs-lookup"><span data-stu-id="fbb90-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb90-623">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbb90-623">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb90-624">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fbb90-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbb90-625">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbb90-625">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb90-626">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fbb90-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbb90-627">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbb90-627">Namespace</span></span><br/>                | <span data-ttu-id="fbb90-628">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fbb90-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbb90-629">MOF</span><span class="sxs-lookup"><span data-stu-id="fbb90-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbb90-630"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbb90-631">DLL</span><span class="sxs-lookup"><span data-stu-id="fbb90-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbb90-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbb90-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

