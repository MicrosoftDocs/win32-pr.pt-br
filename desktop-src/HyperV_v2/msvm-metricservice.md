---
description: Fornece a capacidade de gerenciar métricas.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758641"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="410be-103">\_Classe Msvm MetricService</span><span class="sxs-lookup"><span data-stu-id="410be-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="410be-104">Fornece a capacidade de gerenciar métricas.</span><span class="sxs-lookup"><span data-stu-id="410be-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="410be-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="410be-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="410be-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="410be-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="410be-107">Membros</span><span class="sxs-lookup"><span data-stu-id="410be-107">Members</span></span>

<span data-ttu-id="410be-108">A classe **Msvm \_ MetricService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="410be-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="410be-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="410be-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="410be-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="410be-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="410be-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="410be-111">Methods</span></span>

<span data-ttu-id="410be-112">A classe **Msvm \_ MetricService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="410be-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="410be-113">Método</span><span class="sxs-lookup"><span data-stu-id="410be-113">Method</span></span>                                                                    | <span data-ttu-id="410be-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="410be-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="410be-115">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="410be-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="410be-116">Usado para controlar a coleção de métricas para um elemento ou elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="410be-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="410be-117">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="410be-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="410be-118">Controla as métricas por classe.</span><span class="sxs-lookup"><span data-stu-id="410be-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="410be-119">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="410be-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="410be-120">Define os tempos de exemplo de controle.</span><span class="sxs-lookup"><span data-stu-id="410be-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="410be-121">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="410be-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="410be-122">Recupera os valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="410be-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="410be-123">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="410be-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="410be-124">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="410be-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="410be-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="410be-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="410be-126">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="410be-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="410be-127">**Permétricas**</span><span class="sxs-lookup"><span data-stu-id="410be-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="410be-128">Mostra as métricas especificadas.</span><span class="sxs-lookup"><span data-stu-id="410be-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="410be-129">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="410be-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="410be-130">Mostra as métricas por classe.</span><span class="sxs-lookup"><span data-stu-id="410be-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="410be-131">**StartService**</span><span class="sxs-lookup"><span data-stu-id="410be-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="410be-132">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="410be-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="410be-133">**StopService**</span><span class="sxs-lookup"><span data-stu-id="410be-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="410be-134">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="410be-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="410be-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="410be-135">Properties</span></span>

<span data-ttu-id="410be-136">A classe **Msvm \_ MetricService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="410be-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="410be-137">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="410be-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-138">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="410be-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-140">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="410be-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="410be-141">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="410be-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="410be-142">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="410be-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-145">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="410be-145">A short description of the object.</span></span> <span data-ttu-id="410be-146">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="410be-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="410be-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="410be-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-150">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="410be-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="410be-151">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="410be-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="410be-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="410be-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="410be-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="410be-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="410be-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="410be-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="410be-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="410be-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="410be-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="410be-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="410be-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="410be-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="410be-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="410be-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="410be-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="410be-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="410be-160">)</span><span class="sxs-lookup"><span data-stu-id="410be-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="410be-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="410be-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-164">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="410be-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="410be-165">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ MetricService".</span><span class="sxs-lookup"><span data-stu-id="410be-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="410be-166">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="410be-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-169">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="410be-169">A description of the object.</span></span> <span data-ttu-id="410be-170">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "fornece gerenciamento WMI de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="410be-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="410be-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="410be-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-174">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="410be-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="410be-175">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="410be-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="410be-176">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="410be-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="410be-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="410be-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="410be-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="410be-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="410be-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="410be-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="410be-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="410be-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="410be-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="410be-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="410be-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="410be-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="410be-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="410be-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="410be-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="410be-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="410be-185">)</span><span class="sxs-lookup"><span data-stu-id="410be-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="410be-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="410be-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-189">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="410be-189">A display name for the object.</span></span> <span data-ttu-id="410be-190">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="410be-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="410be-191">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="410be-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-192">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-194">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="410be-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="410be-195">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="410be-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="410be-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="410be-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-199">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="410be-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="410be-200">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="410be-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="410be-201">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="410be-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="410be-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="410be-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-203">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-205">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="410be-205">The current health of the element.</span></span> <span data-ttu-id="410be-206">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="410be-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="410be-207">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="410be-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="410be-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="410be-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="410be-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="410be-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-210">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="410be-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="410be-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-212">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="410be-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="410be-213">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="410be-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="410be-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="410be-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="410be-217">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="410be-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="410be-218">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="410be-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="410be-219">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="410be-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="410be-220">**Nome**</span><span class="sxs-lookup"><span data-stu-id="410be-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-223">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="410be-223">The label by which the object is known.</span></span> <span data-ttu-id="410be-224">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "metricsvc".</span><span class="sxs-lookup"><span data-stu-id="410be-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="410be-225">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="410be-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-226">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-228">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="410be-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="410be-229">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="410be-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="410be-230">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="410be-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="410be-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="410be-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="410be-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="410be-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="410be-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="410be-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="410be-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="410be-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="410be-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="410be-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="410be-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="410be-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="410be-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="410be-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="410be-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="410be-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="410be-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="410be-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="410be-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="410be-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="410be-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="410be-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="410be-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="410be-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="410be-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="410be-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="410be-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="410be-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="410be-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="410be-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="410be-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="410be-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="410be-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="410be-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="410be-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="410be-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="410be-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="410be-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="410be-250">)</span><span class="sxs-lookup"><span data-stu-id="410be-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="410be-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="410be-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-252">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="410be-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-254">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="410be-254">The current statuses of the object.</span></span> <span data-ttu-id="410be-255">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="410be-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="410be-256">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="410be-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-259">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="410be-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="410be-260">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="410be-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="410be-261">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="410be-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="410be-262">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="410be-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-265">Um valor que fornece informações sobre como o proprietário principal do serviço pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="410be-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="410be-266">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="410be-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="410be-267">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="410be-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-270">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="410be-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="410be-271">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="410be-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="410be-272">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="410be-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="410be-273">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="410be-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-274">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-276">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="410be-276">Provides high level status information.</span></span> <span data-ttu-id="410be-277">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="410be-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="410be-278">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="410be-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="410be-279">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="410be-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="410be-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="410be-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="410be-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="410be-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="410be-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="410be-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="410be-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="410be-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="410be-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="410be-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="410be-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="410be-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="410be-286">)</span><span class="sxs-lookup"><span data-stu-id="410be-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="410be-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="410be-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-288">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-290">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="410be-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="410be-291">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="410be-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="410be-292">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="410be-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="410be-293">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="410be-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="410be-294">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="410be-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="410be-295">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="410be-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="410be-296">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="410be-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-297">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="410be-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="410be-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-299">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="410be-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="410be-300">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="410be-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="410be-301">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="410be-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-304">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="410be-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="410be-305">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="410be-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="410be-306">**Status**</span><span class="sxs-lookup"><span data-stu-id="410be-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-309">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="410be-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="410be-310">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="410be-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-311">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="410be-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-313">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="410be-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="410be-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e as cadeias de caracteres são sempre definidas como "OK".</span><span class="sxs-lookup"><span data-stu-id="410be-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="410be-315">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="410be-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-318">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="410be-318">The scoping system's creation class name.</span></span> <span data-ttu-id="410be-319">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="410be-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="410be-320">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="410be-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="410be-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="410be-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-323">O nome do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="410be-323">The name of the hosting computer system.</span></span> <span data-ttu-id="410be-324">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="410be-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="410be-325">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="410be-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-326">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="410be-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="410be-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-328">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="410be-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="410be-329">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="410be-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="410be-330">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="410be-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="410be-331">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="410be-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="410be-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="410be-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="410be-333">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="410be-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="410be-334">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="410be-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="410be-335">Requisitos</span><span class="sxs-lookup"><span data-stu-id="410be-335">Requirements</span></span>



| <span data-ttu-id="410be-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="410be-336">Requirement</span></span> | <span data-ttu-id="410be-337">Valor</span><span class="sxs-lookup"><span data-stu-id="410be-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410be-338">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="410be-338">Minimum supported client</span></span><br/> | <span data-ttu-id="410be-339">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="410be-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="410be-340">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="410be-340">Minimum supported server</span></span><br/> | <span data-ttu-id="410be-341">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="410be-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="410be-342">Namespace</span><span class="sxs-lookup"><span data-stu-id="410be-342">Namespace</span></span><br/>                | <span data-ttu-id="410be-343">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="410be-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="410be-344">MOF</span><span class="sxs-lookup"><span data-stu-id="410be-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="410be-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="410be-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="410be-346">DLL</span><span class="sxs-lookup"><span data-stu-id="410be-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="410be-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="410be-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

