---
description: Representa um evento que é gerado cada vez que a propriedade OperationalStatus da \_ classe Msvm ResourcePool ou Msvm \_ LogicalDisk é alterada.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Classe Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011308"
---
# <a name="msvm_storagealert-class"></a><span data-ttu-id="1a31c-103">\_Classe Msvm StorageAlert</span><span class="sxs-lookup"><span data-stu-id="1a31c-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="1a31c-104">Representa um evento que é gerado cada vez que a propriedade **OperationalStatus** da classe [**Msvm \_ ResourcePool**](msvm-resourcepool.md) ou [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) é alterada.</span><span class="sxs-lookup"><span data-stu-id="1a31c-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="1a31c-105">A sintaxe a seguir é simplificada do código MOF e inclui essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a31c-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a31c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a31c-106">Syntax</span></span>

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a><span data-ttu-id="1a31c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1a31c-107">Members</span></span>

<span data-ttu-id="1a31c-108">A classe **Msvm \_ StorageAlert** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a31c-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="1a31c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a31c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a31c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a31c-110">Properties</span></span>

<span data-ttu-id="1a31c-111">A classe **Msvm \_ StorageAlert** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a31c-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a31c-112">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="1a31c-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a31c-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-115">Qualificadores: **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")</span><span class="sxs-lookup"><span data-stu-id="1a31c-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-116">Especifica o formato da propriedade **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="1a31c-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="1a31c-117">O formato é um CIMObjectPath, com o formato *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\*", que especifica uma instância no esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="1a31c-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="1a31c-118">Essa propriedade é herdada da classe **CIM \_ AlertIndication** .</span><span class="sxs-lookup"><span data-stu-id="1a31c-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="1a31c-119">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="1a31c-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="1a31c-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1a31c-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1a31c-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="1a31c-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a31c-123">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1a31c-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-124">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a31c-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-126">Os caminhos WMI da instância para a qual o alerta é gerado.</span><span class="sxs-lookup"><span data-stu-id="1a31c-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="1a31c-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a31c-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-130">Especifica a classificação primária do alerta.</span><span class="sxs-lookup"><span data-stu-id="1a31c-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="1a31c-131">Os valores possíveis para essa propriedade são:</span><span class="sxs-lookup"><span data-stu-id="1a31c-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="1a31c-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de qualidade de serviço** (3)</span><span class="sxs-lookup"><span data-stu-id="1a31c-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a31c-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="1a31c-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-134">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a31c-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-136">A data e a hora em que o evento subjacente foi detectado.</span><span class="sxs-lookup"><span data-stu-id="1a31c-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-137">**Message**</span><span class="sxs-lookup"><span data-stu-id="1a31c-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a31c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-140">Uma mensagem formatada que é construída pela combinação de alguns ou de todos os elementos dinâmicos especificados na propriedade **MessageArguments** com os elementos estáticos exclusivamente identificados pela propriedade **MessageId** em um registro de mensagem ou outro catálogo associado à propriedade **OwningEntity** .</span><span class="sxs-lookup"><span data-stu-id="1a31c-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-141">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="1a31c-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-142">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a31c-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-144">Uma matriz que contém o conteúdo dinâmico da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a31c-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="1a31c-145">Se o valor de **MessageId** for 32930, o argumento na posição 0 será o **poolid** da instância [**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md) para a qual o alerta é gerado.</span><span class="sxs-lookup"><span data-stu-id="1a31c-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-146">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="1a31c-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a31c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-149">Identifica exclusivamente, dentro do escopo da propriedade **OwningEntity** , o formato da propriedade **Message** .</span><span class="sxs-lookup"><span data-stu-id="1a31c-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="1a31c-150">Os valores possíveis para essa propriedade são:</span><span class="sxs-lookup"><span data-stu-id="1a31c-150">The possible values for this property are:</span></span>

<span data-ttu-id="1a31c-151">32930 ("mensagem de taxa de transferência insuficiente do QoS do pool de armazenamento")</span><span class="sxs-lookup"><span data-stu-id="1a31c-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-152">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="1a31c-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a31c-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-155">Uma cadeia de caracteres que define "other" valores para **AlertingManagedElement**.</span><span class="sxs-lookup"><span data-stu-id="1a31c-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="1a31c-156">Esse valor deve ser definido como um valor não nulo quando **AlertingManagedElement** é definido como um valor de 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="1a31c-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="1a31c-157">Para todos os outros valores de **AlertingManagedElement**, o valor dessa cadeia de caracteres deve ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="1a31c-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="1a31c-158">Essa propriedade é herdada da classe **CIM \_ AlertIndication** .</span><span class="sxs-lookup"><span data-stu-id="1a31c-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-159">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="1a31c-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a31c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-162">Identifica exclusivamente a entidade que possui a definição do formato da **mensagem** descrita nesta instância.</span><span class="sxs-lookup"><span data-stu-id="1a31c-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="1a31c-163">O valor dessa propriedade é sempre "Microsoft-Windows-Hyper-V."</span><span class="sxs-lookup"><span data-stu-id="1a31c-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="1a31c-164">"Microsoft-Windows-Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="1a31c-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="1a31c-165">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="1a31c-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-166">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a31c-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-168">Descreve a severidade da indicação de alerta.</span><span class="sxs-lookup"><span data-stu-id="1a31c-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="1a31c-169">Os valores possíveis para essa propriedade são:</span><span class="sxs-lookup"><span data-stu-id="1a31c-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="1a31c-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)</span><span class="sxs-lookup"><span data-stu-id="1a31c-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/aviso** (3)</span><span class="sxs-lookup"><span data-stu-id="1a31c-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a31c-172">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="1a31c-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-173">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a31c-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-175">Descreve a causa provável da situação que resultou na indicação de alerta.</span><span class="sxs-lookup"><span data-stu-id="1a31c-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="1a31c-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema de capacidade de armazenamento** (50)</span><span class="sxs-lookup"><span data-stu-id="1a31c-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior limpo** (59)</span><span class="sxs-lookup"><span data-stu-id="1a31c-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a31c-178">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="1a31c-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a31c-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a31c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a31c-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a31c-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a31c-181">Uma descrição textual que corresponde ao valor da propriedade **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="1a31c-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a31c-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a31c-182">Remarks</span></span>

<span data-ttu-id="1a31c-183">O provedor WMI do Hyper-V não gerará eventos para discos virtuais individuais para evitar a inundação de clientes com eventos em caso de problemas de grande escala dos sistemas de armazenamento subjacentes.</span><span class="sxs-lookup"><span data-stu-id="1a31c-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="1a31c-184">Quando um cliente recebe um evento **Msvm \_ StorageAlert** , se o valor da propriedade **ProbableCause** for 50 (problema de capacidade de armazenamento), o cliente poderá descobrir quais discos virtuais estão operando fora de sua política de QoS usando um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1a31c-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="1a31c-185">Consulte todas as instâncias do [**\_ LogicalDisk Msvm**](msvm-logicaldisk.md) que foram alocadas do pool de recursos para o qual o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="1a31c-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="1a31c-186">Essas instâncias do **Msvm \_ LogicalDisk** estão associadas ao pool de recursos por meio da Associação [**Msvm \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) .</span><span class="sxs-lookup"><span data-stu-id="1a31c-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="1a31c-187">Filtre a lista de resultados selecionando instâncias cujo OperationalStatus contém taxa de transferência insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1a31c-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="1a31c-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a31c-188">Requirements</span></span>



| <span data-ttu-id="1a31c-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a31c-189">Requirement</span></span> | <span data-ttu-id="1a31c-190">Valor</span><span class="sxs-lookup"><span data-stu-id="1a31c-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a31c-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a31c-191">Minimum supported client</span></span><br/> | <span data-ttu-id="1a31c-192">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a31c-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1a31c-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a31c-193">Minimum supported server</span></span><br/> | <span data-ttu-id="1a31c-194">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="1a31c-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1a31c-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a31c-195">Namespace</span></span><br/>                | <span data-ttu-id="1a31c-196">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1a31c-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1a31c-197">MOF</span><span class="sxs-lookup"><span data-stu-id="1a31c-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a31c-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a31c-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a31c-199">DLL</span><span class="sxs-lookup"><span data-stu-id="1a31c-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a31c-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a31c-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a31c-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a31c-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a31c-202">**\_ALERTINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="1a31c-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="1a31c-203">**\_LogicalDisk Msvm**</span><span class="sxs-lookup"><span data-stu-id="1a31c-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="1a31c-204">**Msvm \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="1a31c-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




