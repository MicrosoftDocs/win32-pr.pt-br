---
description: Representa uma porta no comutador de Fibre Channel virtual.
ms.assetid: 6b4553b7-2717-4285-9e1a-e2ad22a60997
title: Classe Msvm_FcSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcSwitchPort
- Msvm_FcSwitchPort.SetPowerState
- Msvm_FcSwitchPort.EnableDevice
- Msvm_FcSwitchPort.OnlineDevice
- Msvm_FcSwitchPort.QuiesceDevice
- Msvm_FcSwitchPort.SaveProperties
- Msvm_FcSwitchPort.RestoreProperties
- Msvm_FcSwitchPort.InstanceID
- Msvm_FcSwitchPort.Caption
- Msvm_FcSwitchPort.Description
- Msvm_FcSwitchPort.ElementName
- Msvm_FcSwitchPort.InstallDate
- Msvm_FcSwitchPort.Name
- Msvm_FcSwitchPort.OperationalStatus
- Msvm_FcSwitchPort.StatusDescriptions
- Msvm_FcSwitchPort.Status
- Msvm_FcSwitchPort.HealthState
- Msvm_FcSwitchPort.CommunicationStatus
- Msvm_FcSwitchPort.DetailedStatus
- Msvm_FcSwitchPort.OperatingStatus
- Msvm_FcSwitchPort.PrimaryStatus
- Msvm_FcSwitchPort.EnabledState
- Msvm_FcSwitchPort.OtherEnabledState
- Msvm_FcSwitchPort.RequestedState
- Msvm_FcSwitchPort.EnabledDefault
- Msvm_FcSwitchPort.TimeOfLastStateChange
- Msvm_FcSwitchPort.AvailableRequestedStates
- Msvm_FcSwitchPort.TransitioningToState
- Msvm_FcSwitchPort.SystemCreationClassName
- Msvm_FcSwitchPort.SystemName
- Msvm_FcSwitchPort.CreationClassName
- Msvm_FcSwitchPort.DeviceID
- Msvm_FcSwitchPort.PowerManagementSupported
- Msvm_FcSwitchPort.PowerManagementCapabilities
- Msvm_FcSwitchPort.Availability
- Msvm_FcSwitchPort.StatusInfo
- Msvm_FcSwitchPort.LastErrorCode
- Msvm_FcSwitchPort.ErrorDescription
- Msvm_FcSwitchPort.ErrorCleared
- Msvm_FcSwitchPort.OtherIdentifyingInfo
- Msvm_FcSwitchPort.PowerOnHours
- Msvm_FcSwitchPort.TotalPowerOnHours
- Msvm_FcSwitchPort.IdentifyingDescriptions
- Msvm_FcSwitchPort.AdditionalAvailability
- Msvm_FcSwitchPort.MaxQuiesceTime
- Msvm_FcSwitchPort.Speed
- Msvm_FcSwitchPort.MaxSpeed
- Msvm_FcSwitchPort.RequestedSpeed
- Msvm_FcSwitchPort.UsageRestriction
- Msvm_FcSwitchPort.PortType
- Msvm_FcSwitchPort.OtherPortType
- Msvm_FcSwitchPort.OtherNetworkPortType
- Msvm_FcSwitchPort.PortNumber
- Msvm_FcSwitchPort.LinkTechnology
- Msvm_FcSwitchPort.OtherLinkTechnology
- Msvm_FcSwitchPort.PermanentAddress
- Msvm_FcSwitchPort.NetworkAddresses
- Msvm_FcSwitchPort.FullDuplex
- Msvm_FcSwitchPort.AutoSense
- Msvm_FcSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_FcSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_FcSwitchPort.SupportedCOS
- Msvm_FcSwitchPort.ActiveCOS
- Msvm_FcSwitchPort.SupportedFC4Types
- Msvm_FcSwitchPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443ae1065b7c7a6a4bb1523a672e388cacb91667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501918"
---
# <a name="msvm_fcswitchport-class"></a><span data-ttu-id="73e99-103">\_Classe Msvm FcSwitchPort</span><span class="sxs-lookup"><span data-stu-id="73e99-103">Msvm\_FcSwitchPort class</span></span>

> [!NOTE]
> <span data-ttu-id="73e99-104">Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="73e99-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="73e99-105">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="73e99-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="73e99-106">Representa uma porta no comutador de Fibre Channel virtual.</span><span class="sxs-lookup"><span data-stu-id="73e99-106">Represents a port on the virtual Fibre Channel switch.</span></span>

<span data-ttu-id="73e99-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="73e99-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e99-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73e99-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcSwitchPort : CIM_FCPort
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
  uint16   LinkTechnology;
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

## <a name="members"></a><span data-ttu-id="73e99-109">Membros</span><span class="sxs-lookup"><span data-stu-id="73e99-109">Members</span></span>

<span data-ttu-id="73e99-110">A classe **Msvm \_ FcSwitchPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="73e99-110">The **Msvm\_FcSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="73e99-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="73e99-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="73e99-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73e99-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73e99-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="73e99-113">Methods</span></span>

<span data-ttu-id="73e99-114">A classe **Msvm \_ FcSwitchPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="73e99-114">The **Msvm\_FcSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="73e99-115">Método</span><span class="sxs-lookup"><span data-stu-id="73e99-115">Method</span></span>                                                             | <span data-ttu-id="73e99-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="73e99-116">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="73e99-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="73e99-117">**EnableDevice**</span></span>                                                   | <span data-ttu-id="73e99-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="73e99-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73e99-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="73e99-119">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="73e99-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="73e99-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73e99-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="73e99-121">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="73e99-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="73e99-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="73e99-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="73e99-123">**RequestStateChange**</span></span>](msvm-fcswitchport-requeststatechange.md) | <span data-ttu-id="73e99-124">solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="73e99-124">requests a state change.</span></span><br/>      |
| [<span data-ttu-id="73e99-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="73e99-125">**Reset**</span></span>](msvm-fcswitchport-reset.md)                           | <span data-ttu-id="73e99-126">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="73e99-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="73e99-127">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="73e99-127">**RestoreProperties**</span></span>                                              | <span data-ttu-id="73e99-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="73e99-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73e99-129">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="73e99-129">**SaveProperties**</span></span>                                                 | <span data-ttu-id="73e99-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="73e99-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73e99-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="73e99-131">**SetPowerState**</span></span>                                                  | <span data-ttu-id="73e99-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="73e99-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="73e99-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73e99-133">Properties</span></span>

<span data-ttu-id="73e99-134">A classe **Msvm \_ FcSwitchPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="73e99-134">The **Msvm\_FcSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73e99-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="73e99-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-136">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-138">Uma matriz de inteiros que indica as classes de serviço que estão ativas.</span><span class="sxs-lookup"><span data-stu-id="73e99-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="73e99-139">O COS com suporte é especificado pela propriedade **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="73e99-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="73e99-140">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="73e99-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="73e99-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="73e99-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="73e99-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="73e99-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-150">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-152">Uma matriz de inteiros que indica o Fibre Channel protocolos FC-4 em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="73e99-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="73e99-153">Uma lista de todos os protocolos com suporte é especificada pela propriedade **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="73e99-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="73e99-154">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="73e99-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="73e99-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sobre FC** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="73e99-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="73e99-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 mestre** (17)</span><span class="sxs-lookup"><span data-stu-id="73e99-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 escravo** (18)</span><span class="sxs-lookup"><span data-stu-id="73e99-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 par** (19)</span><span class="sxs-lookup"><span data-stu-id="73e99-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="73e99-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 escravo** (22)</span><span class="sxs-lookup"><span data-stu-id="73e99-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 par** (23)</span><span class="sxs-lookup"><span data-stu-id="73e99-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="73e99-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidade de controle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="73e99-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="73e99-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidade de controle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="73e99-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="73e99-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="73e99-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="73e99-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="73e99-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controle bbl** (80)</span><span class="sxs-lookup"><span data-stu-id="73e99-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada bbl FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="73e99-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="73e99-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="73e99-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="73e99-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Exclusivo do fornecedor** (255)</span><span class="sxs-lookup"><span data-stu-id="73e99-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="73e99-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-182">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-184">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="73e99-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73e99-185">A unidade de transmissão máxima (MTU) do negociada ou ativa que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="73e99-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="73e99-186">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="73e99-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-188">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-190">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73e99-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="73e99-191">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-192">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="73e99-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-193">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73e99-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-195">Indica se a porta é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="73e99-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="73e99-196">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-197">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="73e99-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-200">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73e99-200">The primary availability and status of the device.</span></span> <span data-ttu-id="73e99-201">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="73e99-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-203">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-205">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="73e99-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="73e99-206">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="73e99-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-207">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="73e99-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-210">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="73e99-210">A short description of the object.</span></span> <span data-ttu-id="73e99-211">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="73e99-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-215">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="73e99-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="73e99-216">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="73e99-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73e99-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="73e99-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73e99-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73e99-225">)</span><span class="sxs-lookup"><span data-stu-id="73e99-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73e99-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-229">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="73e99-229">The scoping system's creation class name.</span></span> <span data-ttu-id="73e99-230">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73e99-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-231">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="73e99-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-234">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="73e99-234">A description of the object.</span></span> <span data-ttu-id="73e99-235">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="73e99-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-239">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="73e99-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="73e99-240">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="73e99-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73e99-241">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="73e99-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73e99-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73e99-250">)</span><span class="sxs-lookup"><span data-stu-id="73e99-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="73e99-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-254">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="73e99-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="73e99-255">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73e99-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="73e99-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-259">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="73e99-259">A display name for the object.</span></span> <span data-ttu-id="73e99-260">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="73e99-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-262">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-264">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="73e99-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="73e99-265">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="73e99-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="73e99-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-269">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="73e99-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="73e99-270">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="73e99-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="73e99-271">Valor</span><span class="sxs-lookup"><span data-stu-id="73e99-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="73e99-272">Significado</span><span class="sxs-lookup"><span data-stu-id="73e99-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="73e99-273"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="73e99-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="73e99-274">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="73e99-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="73e99-275"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="73e99-276"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="73e99-277">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="73e99-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="73e99-278"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="73e99-279">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="73e99-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="73e99-280"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="73e99-281">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="73e99-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="73e99-282"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="73e99-283">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="73e99-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="73e99-284"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="73e99-285">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="73e99-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="73e99-286"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="73e99-287">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="73e99-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="73e99-288"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="73e99-289">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="73e99-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="73e99-290"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="73e99-291">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="73e99-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="73e99-292">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="73e99-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="73e99-293">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="73e99-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="73e99-294"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="73e99-295">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="73e99-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="73e99-296">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="73e99-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="73e99-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="73e99-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-298">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73e99-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-300">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="73e99-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="73e99-301">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="73e99-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-305">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="73e99-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="73e99-306">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="73e99-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-308">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73e99-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-310">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="73e99-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="73e99-311">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="73e99-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-313">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-315">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="73e99-315">The current health of the element.</span></span> <span data-ttu-id="73e99-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="73e99-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-318">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-320">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="73e99-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="73e99-321">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73e99-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-323">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73e99-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-325">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="73e99-325">The date and time when the object was installed.</span></span> <span data-ttu-id="73e99-326">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="73e99-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="73e99-327">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="73e99-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-331">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="73e99-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="73e99-332">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="73e99-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="73e99-333">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="73e99-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73e99-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-337">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="73e99-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="73e99-338">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="73e99-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-340">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-342">Especifica o tipo de tecnologia de link para a porta.</span><span class="sxs-lookup"><span data-stu-id="73e99-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="73e99-343">Quando definido como 1 (outro), a propriedade **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="73e99-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="73e99-344">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="73e99-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="73e99-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="73e99-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infravermelho** (9)</span><span class="sxs-lookup"><span data-stu-id="73e99-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="73e99-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN sem fio** (11)</span><span class="sxs-lookup"><span data-stu-id="73e99-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-357">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="73e99-357">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-358">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-360">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="73e99-360">This property has been deprecated.</span></span> <span data-ttu-id="73e99-361">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-362">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="73e99-362">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-363">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-365">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="73e99-365">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="73e99-366">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="73e99-366">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="73e99-367">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e99-367">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-368">**Nome**</span><span class="sxs-lookup"><span data-stu-id="73e99-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-371">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="73e99-371">The label by which the object is known.</span></span> <span data-ttu-id="73e99-372">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-373">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="73e99-373">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-374">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-374">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-376">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="73e99-376">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="73e99-377">Uma matriz de cadeias de caracteres que contêm os endereços MAC para a porta.</span><span class="sxs-lookup"><span data-stu-id="73e99-377">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="73e99-378">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-378">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-379">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="73e99-379">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-380">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-382">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="73e99-382">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="73e99-383">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="73e99-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73e99-384">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="73e99-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="73e99-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="73e99-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="73e99-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="73e99-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="73e99-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="73e99-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="73e99-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="73e99-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="73e99-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="73e99-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="73e99-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73e99-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73e99-404">)</span><span class="sxs-lookup"><span data-stu-id="73e99-404">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-405">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="73e99-405">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-406">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-408">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="73e99-408">The current statuses of the object.</span></span> <span data-ttu-id="73e99-409">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-410">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="73e99-410">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-411">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-413">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="73e99-413">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="73e99-414">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="73e99-414">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="73e99-415">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="73e99-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-416">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="73e99-416">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-417">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-417">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-419">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="73e99-419">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="73e99-420">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-421">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="73e99-421">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-422">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-424">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1, (outro).</span><span class="sxs-lookup"><span data-stu-id="73e99-424">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="73e99-425">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-425">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-426">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="73e99-426">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-429">O uso dessa propriedade é preterido no lugar da propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="73e99-429">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="73e99-430">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-431">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="73e99-431">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-432">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-434">Descreve o tipo de módulo quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="73e99-434">Describes the type of module when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="73e99-435">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e99-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-436">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="73e99-436">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-437">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-439">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="73e99-439">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="73e99-440">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="73e99-440">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="73e99-441">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="73e99-441">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="73e99-442">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="73e99-442">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="73e99-443">Essa propriedade deverá ser **nula** se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="73e99-443">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="73e99-444">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-444">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-445">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="73e99-445">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-446">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-448">O número da porta.</span><span class="sxs-lookup"><span data-stu-id="73e99-448">The port number.</span></span> <span data-ttu-id="73e99-449">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-450">**PortType**</span><span class="sxs-lookup"><span data-stu-id="73e99-450">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-451">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-453">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="73e99-453">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="73e99-454">Quando definido como 1 (outro), a propriedade **OtherPortType** relacionada contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="73e99-454">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="73e99-455">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e99-455">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>+ **/50 10BaseT de cobre** (50)</span><span class="sxs-lookup"><span data-stu-id="73e99-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="73e99-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="73e99-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="73e99-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="73e99-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="73e99-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="73e99-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="73e99-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="73e99-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="73e99-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="73e99-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="73e99-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="73e99-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="73e99-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="73e99-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="73e99-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="73e99-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="73e99-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="73e99-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="73e99-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-478">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="73e99-478">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-479">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-479">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-481">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73e99-481">The power management capabilities of the device.</span></span> <span data-ttu-id="73e99-482">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-482">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-483">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="73e99-483">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-484">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73e99-484">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-485">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-486">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="73e99-486">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="73e99-487">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-488">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="73e99-488">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-489">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-489">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-491">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="73e99-491">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="73e99-492">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-493">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="73e99-493">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-494">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-496">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="73e99-496">Provides high level status information.</span></span> <span data-ttu-id="73e99-497">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="73e99-497">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="73e99-498">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="73e99-498">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73e99-499">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-499">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="73e99-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73e99-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73e99-506">)</span><span class="sxs-lookup"><span data-stu-id="73e99-506">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-507">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="73e99-507">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-508">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-509">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="73e99-509">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-510">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="73e99-510">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="73e99-511">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="73e99-511">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="73e99-512">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="73e99-512">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="73e99-513">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e99-513">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-514">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="73e99-514">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-515">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-516">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-517">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="73e99-517">The last requested or desired state for the element.</span></span> <span data-ttu-id="73e99-518">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="73e99-518">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-519">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="73e99-519">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-520">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-520">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-521">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-522">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="73e99-522">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="73e99-523">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="73e99-523">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="73e99-524">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e99-524">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-525">**Status**</span><span class="sxs-lookup"><span data-stu-id="73e99-525">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-526">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-527">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-528">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="73e99-528">The current status of the object.</span></span> <span data-ttu-id="73e99-529">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="73e99-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-531">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-532">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-533">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="73e99-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="73e99-534">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73e99-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-535">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="73e99-535">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-536">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-537">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-538">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="73e99-538">The current state of the logical device.</span></span> <span data-ttu-id="73e99-539">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-539">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-540">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="73e99-540">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-541">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-543">Uma matriz de inteiros que indica o Fibre Channel classes de serviço (COS) que têm suporte.</span><span class="sxs-lookup"><span data-stu-id="73e99-543">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="73e99-544">O COS ativo é especificado pela propriedade **ActiveCOS** .</span><span class="sxs-lookup"><span data-stu-id="73e99-544">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="73e99-545">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="73e99-545">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="73e99-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-547"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-547"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-548"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-548"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-549"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-549"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-550"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-550"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-551"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-551"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-552"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="73e99-552"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-553"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="73e99-553"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-554">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="73e99-554">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-555">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-555">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73e99-556">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-557">Uma matriz de inteiros que indica o Fibre Channel protocolos FC-4 com suporte.</span><span class="sxs-lookup"><span data-stu-id="73e99-557">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="73e99-558">Os protocolos que estão ativos e em execução são especificados pela propriedade **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="73e99-558">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="73e99-559">Essa propriedade é herdada do **CIM \_ FCPort**.</span><span class="sxs-lookup"><span data-stu-id="73e99-559">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="73e99-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73e99-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sobre FC** (5)</span><span class="sxs-lookup"><span data-stu-id="73e99-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="73e99-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="73e99-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 mestre** (17)</span><span class="sxs-lookup"><span data-stu-id="73e99-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 escravo** (18)</span><span class="sxs-lookup"><span data-stu-id="73e99-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 par** (19)</span><span class="sxs-lookup"><span data-stu-id="73e99-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="73e99-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 escravo** (22)</span><span class="sxs-lookup"><span data-stu-id="73e99-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 par** (23)</span><span class="sxs-lookup"><span data-stu-id="73e99-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="73e99-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidade de controle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="73e99-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="73e99-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidade de controle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="73e99-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="73e99-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="73e99-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="73e99-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="73e99-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controle bbl** (80)</span><span class="sxs-lookup"><span data-stu-id="73e99-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada bbl FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="73e99-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="73e99-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="73e99-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="73e99-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Exclusivo do fornecedor** (255)</span><span class="sxs-lookup"><span data-stu-id="73e99-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e99-586">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="73e99-586">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-587">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-587">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-588">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e99-589">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="73e99-589">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73e99-590">A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="73e99-590">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="73e99-591">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="73e99-591">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-592">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73e99-592">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-593">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-593">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-594">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-594">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-595">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="73e99-595">The scoping system's creation class name.</span></span> <span data-ttu-id="73e99-596">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73e99-596">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-597">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="73e99-597">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-598">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73e99-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-599">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-600">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="73e99-600">The scoping system's name.</span></span> <span data-ttu-id="73e99-601">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73e99-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73e99-602">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="73e99-602">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-603">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73e99-603">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-604">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-605">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="73e99-605">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="73e99-606">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="73e99-606">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-607">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="73e99-607">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-608">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73e99-608">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-609">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-610">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="73e99-610">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="73e99-611">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="73e99-611">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-612">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="73e99-612">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-613">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-614">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-615">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="73e99-615">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="73e99-616">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="73e99-616">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73e99-617">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="73e99-617">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e99-618">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73e99-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73e99-619">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73e99-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73e99-620">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="73e99-620">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="73e99-621">Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts.</span><span class="sxs-lookup"><span data-stu-id="73e99-621">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="73e99-622">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="73e99-622">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="73e99-623">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e99-623">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="73e99-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73e99-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Somente front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="73e99-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Somente back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="73e99-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73e99-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Não restrito** (4)</span><span class="sxs-lookup"><span data-stu-id="73e99-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73e99-628">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73e99-628">Requirements</span></span>



| <span data-ttu-id="73e99-629">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e99-629">Requirement</span></span> | <span data-ttu-id="73e99-630">Valor</span><span class="sxs-lookup"><span data-stu-id="73e99-630">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e99-631">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73e99-631">Minimum supported client</span></span><br/> | <span data-ttu-id="73e99-632">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="73e99-632">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="73e99-633">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73e99-633">Minimum supported server</span></span><br/> | <span data-ttu-id="73e99-634">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="73e99-634">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73e99-635">Namespace</span><span class="sxs-lookup"><span data-stu-id="73e99-635">Namespace</span></span><br/>                | <span data-ttu-id="73e99-636">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="73e99-636">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="73e99-637">MOF</span><span class="sxs-lookup"><span data-stu-id="73e99-637">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73e99-638"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-638"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73e99-639">DLL</span><span class="sxs-lookup"><span data-stu-id="73e99-639">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73e99-640"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73e99-640"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

