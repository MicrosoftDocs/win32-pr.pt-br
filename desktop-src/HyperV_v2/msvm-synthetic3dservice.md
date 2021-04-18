---
description: Descreve o serviço de GPU 3D sintético.
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758636"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="087ed-103">\_Classe Msvm Synthetic3DService</span><span class="sxs-lookup"><span data-stu-id="087ed-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="087ed-104">Descreve o serviço de GPU 3D sintético.</span><span class="sxs-lookup"><span data-stu-id="087ed-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="087ed-105">Essa classe não está disponível para máquinas virtuais de geração 2.</span><span class="sxs-lookup"><span data-stu-id="087ed-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="087ed-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="087ed-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="087ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="087ed-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
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
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="087ed-108">Membros</span><span class="sxs-lookup"><span data-stu-id="087ed-108">Members</span></span>

<span data-ttu-id="087ed-109">A classe **Msvm \_ Synthetic3DService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="087ed-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="087ed-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="087ed-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="087ed-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="087ed-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="087ed-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="087ed-112">Methods</span></span>

<span data-ttu-id="087ed-113">A classe **Msvm \_ Synthetic3DService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="087ed-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="087ed-114">Método</span><span class="sxs-lookup"><span data-stu-id="087ed-114">Method</span></span>                                                                                     | <span data-ttu-id="087ed-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="087ed-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="087ed-116">**DisableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="087ed-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="087ed-117">Desabilita uma GPU física para virtualização.</span><span class="sxs-lookup"><span data-stu-id="087ed-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="087ed-118">**EnableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="087ed-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="087ed-119">Habilita uma GPU física para virtualização.</span><span class="sxs-lookup"><span data-stu-id="087ed-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="087ed-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="087ed-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="087ed-121">Modifica os dados de configuração para o serviço 3D sintético.</span><span class="sxs-lookup"><span data-stu-id="087ed-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="087ed-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="087ed-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="087ed-123">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="087ed-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="087ed-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="087ed-124">**StartService**</span></span>                                                                           | <span data-ttu-id="087ed-125">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="087ed-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="087ed-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="087ed-126">**StopService**</span></span>                                                                            | <span data-ttu-id="087ed-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="087ed-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="087ed-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="087ed-128">Properties</span></span>

<span data-ttu-id="087ed-129">A classe **Msvm \_ Synthetic3DService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="087ed-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="087ed-130">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="087ed-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-131">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="087ed-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-133">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="087ed-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="087ed-134">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087ed-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-135">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="087ed-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-138">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="087ed-138">A short description of the object.</span></span> <span data-ttu-id="087ed-139">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="087ed-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-143">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="087ed-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="087ed-144">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="087ed-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="087ed-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="087ed-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="087ed-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="087ed-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="087ed-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="087ed-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="087ed-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="087ed-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="087ed-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="087ed-153">)</span><span class="sxs-lookup"><span data-stu-id="087ed-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="087ed-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="087ed-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-157">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="087ed-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="087ed-158">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-159">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="087ed-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-162">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="087ed-162">A description of the object.</span></span> <span data-ttu-id="087ed-163">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="087ed-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-167">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="087ed-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="087ed-168">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="087ed-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="087ed-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="087ed-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="087ed-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="087ed-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="087ed-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="087ed-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="087ed-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="087ed-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="087ed-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="087ed-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="087ed-178">)</span><span class="sxs-lookup"><span data-stu-id="087ed-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="087ed-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="087ed-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-182">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="087ed-182">A display name for the object.</span></span> <span data-ttu-id="087ed-183">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-184">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="087ed-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-185">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-187">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="087ed-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="087ed-188">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087ed-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="087ed-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-192">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="087ed-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="087ed-193">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="087ed-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="087ed-194">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087ed-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="087ed-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-198">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="087ed-198">The current health of the element.</span></span> <span data-ttu-id="087ed-199">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="087ed-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="087ed-200">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="087ed-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="087ed-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="087ed-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-203">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="087ed-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-205">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="087ed-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="087ed-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="087ed-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="087ed-210">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="087ed-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="087ed-211">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="087ed-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="087ed-212">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="087ed-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="087ed-213">**Nome**</span><span class="sxs-lookup"><span data-stu-id="087ed-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-216">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="087ed-216">The label by which the object is known.</span></span> <span data-ttu-id="087ed-217">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-218">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="087ed-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-219">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-221">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="087ed-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="087ed-222">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="087ed-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="087ed-223">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="087ed-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="087ed-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="087ed-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="087ed-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="087ed-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="087ed-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="087ed-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="087ed-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="087ed-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="087ed-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="087ed-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="087ed-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="087ed-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="087ed-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="087ed-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="087ed-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="087ed-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="087ed-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="087ed-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="087ed-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="087ed-243">)</span><span class="sxs-lookup"><span data-stu-id="087ed-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="087ed-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="087ed-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-245">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="087ed-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-247">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="087ed-247">The current statuses of the object.</span></span> <span data-ttu-id="087ed-248">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-249">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="087ed-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-252">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="087ed-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="087ed-253">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="087ed-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="087ed-254">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087ed-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-255">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="087ed-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-258">Um valor que fornece informações sobre como o proprietário principal do serviço pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="087ed-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="087ed-259">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-260">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="087ed-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-263">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="087ed-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="087ed-264">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="087ed-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="087ed-265">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="087ed-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-269">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="087ed-269">Provides high level status information.</span></span> <span data-ttu-id="087ed-270">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="087ed-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="087ed-271">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="087ed-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="087ed-272">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="087ed-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="087ed-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="087ed-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="087ed-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="087ed-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="087ed-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="087ed-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="087ed-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="087ed-279">)</span><span class="sxs-lookup"><span data-stu-id="087ed-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="087ed-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="087ed-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-281">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-283">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="087ed-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="087ed-284">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="087ed-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="087ed-285">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="087ed-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="087ed-286">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="087ed-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="087ed-287">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="087ed-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="087ed-288">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="087ed-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="087ed-289">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="087ed-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-290">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="087ed-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-292">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="087ed-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="087ed-293">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-294">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="087ed-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-297">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="087ed-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="087ed-298">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-299">**Status**</span><span class="sxs-lookup"><span data-stu-id="087ed-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-302">O status do elemento.</span><span class="sxs-lookup"><span data-stu-id="087ed-302">The status of the element.</span></span> <span data-ttu-id="087ed-303">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-304">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="087ed-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-305">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="087ed-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-307">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="087ed-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="087ed-308">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="087ed-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-309">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="087ed-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-312">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="087ed-312">The scoping system's creation class name.</span></span> <span data-ttu-id="087ed-313">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-314">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="087ed-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="087ed-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-317">O nome do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="087ed-317">The name of the hosting computer system.</span></span> <span data-ttu-id="087ed-318">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="087ed-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-319">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="087ed-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-320">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="087ed-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-322">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="087ed-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="087ed-323">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087ed-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="087ed-324">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="087ed-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="087ed-325">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="087ed-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="087ed-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="087ed-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="087ed-327">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="087ed-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="087ed-328">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="087ed-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="087ed-329">Requisitos</span><span class="sxs-lookup"><span data-stu-id="087ed-329">Requirements</span></span>



| <span data-ttu-id="087ed-330">Requisito</span><span class="sxs-lookup"><span data-stu-id="087ed-330">Requirement</span></span> | <span data-ttu-id="087ed-331">Valor</span><span class="sxs-lookup"><span data-stu-id="087ed-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="087ed-332">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="087ed-332">Minimum supported client</span></span><br/> | <span data-ttu-id="087ed-333">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="087ed-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="087ed-334">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="087ed-334">Minimum supported server</span></span><br/> | <span data-ttu-id="087ed-335">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="087ed-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="087ed-336">Namespace</span><span class="sxs-lookup"><span data-stu-id="087ed-336">Namespace</span></span><br/>                | <span data-ttu-id="087ed-337">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="087ed-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="087ed-338">MOF</span><span class="sxs-lookup"><span data-stu-id="087ed-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="087ed-339"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="087ed-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="087ed-340">DLL</span><span class="sxs-lookup"><span data-stu-id="087ed-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="087ed-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="087ed-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

