---
description: Uma versão concreta da classe de \_ trabalho do CIM. Essa classe representa uma unidade de trabalho instanciáveis genérica a ser executada, como um lote ou um trabalho de impressão.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778599"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="93e0c-104">\_Classe CIM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="93e0c-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="93e0c-105">Uma versão concreta da classe [**de \_ trabalho do CIM**](cim-job.md) .</span><span class="sxs-lookup"><span data-stu-id="93e0c-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="93e0c-106">Essa classe representa uma unidade de trabalho instanciáveis genérica a ser executada, como um lote ou um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="93e0c-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e0c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93e0c-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="93e0c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="93e0c-108">Members</span></span>

<span data-ttu-id="93e0c-109">A classe **CIM \_ ConcreteJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="93e0c-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="93e0c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="93e0c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="93e0c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93e0c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93e0c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="93e0c-112">Methods</span></span>

<span data-ttu-id="93e0c-113">A classe **CIM \_ ConcreteJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="93e0c-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="93e0c-114">Método</span><span class="sxs-lookup"><span data-stu-id="93e0c-114">Method</span></span>                                                           | <span data-ttu-id="93e0c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="93e0c-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="93e0c-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="93e0c-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="93e0c-117">Recupera informações de erro para o status operacional de um trabalho concreto.</span><span class="sxs-lookup"><span data-stu-id="93e0c-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="93e0c-118">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="93e0c-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="93e0c-119">Solicita a alteração de estado especificada para um trabalho concreto.</span><span class="sxs-lookup"><span data-stu-id="93e0c-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="93e0c-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93e0c-120">Properties</span></span>

<span data-ttu-id="93e0c-121">A classe **CIM \_ ConcreteJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="93e0c-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93e0c-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93e0c-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93e0c-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93e0c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93e0c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-125">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="93e0c-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="93e0c-126">Identifica exclusivamente e de forma opaca uma instância dessa classe dentro do escopo do namespace que a contém.</span><span class="sxs-lookup"><span data-stu-id="93e0c-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="93e0c-127">Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="93e0c-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="93e0c-128">*OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="93e0c-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="93e0c-129">Esse padrão é semelhante à estrutura de nomes de classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="93e0c-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="93e0c-130">Além disso, para garantir a exclusividade, os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="93e0c-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="93e0c-131">Portanto, o *OrgID* não deve conter dois-pontos (': ').</span><span class="sxs-lookup"><span data-stu-id="93e0c-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="93e0c-132">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.</span><span class="sxs-lookup"><span data-stu-id="93e0c-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="93e0c-133">Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="93e0c-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="93e0c-134">Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="93e0c-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="93e0c-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="93e0c-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93e0c-136">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93e0c-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93e0c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93e0c-138">O estado operacional do trabalho e a transição entre esses Estados.</span><span class="sxs-lookup"><span data-stu-id="93e0c-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="93e0c-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**Novo** (2)</span><span class="sxs-lookup"><span data-stu-id="93e0c-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-140">o trabalho nunca foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="93e0c-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="93e0c-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="93e0c-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-142">O trabalho está sendo movido dos Estados ' novo ', ' suspenso ' ou ' serviço ' para o estado ' em execução '.</span><span class="sxs-lookup"><span data-stu-id="93e0c-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="93e0c-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (4)</span><span class="sxs-lookup"><span data-stu-id="93e0c-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-144">O trabalho está em execução.</span><span class="sxs-lookup"><span data-stu-id="93e0c-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="93e0c-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (5)</span><span class="sxs-lookup"><span data-stu-id="93e0c-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-146">O trabalho é interrompido, mas pode ser reiniciado de maneira direta.</span><span class="sxs-lookup"><span data-stu-id="93e0c-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="93e0c-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (6)</span><span class="sxs-lookup"><span data-stu-id="93e0c-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-148">O trabalho está mudando para um estado ' Concluído ', ' encerrado ' ou ' eliminado '.</span><span class="sxs-lookup"><span data-stu-id="93e0c-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="93e0c-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (7)</span><span class="sxs-lookup"><span data-stu-id="93e0c-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-150">O trabalho foi concluído normalmente.</span><span class="sxs-lookup"><span data-stu-id="93e0c-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="93e0c-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (8)</span><span class="sxs-lookup"><span data-stu-id="93e0c-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-152">O trabalho foi interrompido por uma solicitação de alteração de estado ' Terminate '.</span><span class="sxs-lookup"><span data-stu-id="93e0c-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="93e0c-153">O trabalho e todos os seus processos subjacentes são encerrados e podem ser reiniciados (isso é específico do trabalho) somente como um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="93e0c-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="93e0c-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Eliminado** (9)</span><span class="sxs-lookup"><span data-stu-id="93e0c-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-155">O trabalho foi interrompido por uma solicitação de alteração de estado ' Kill '.</span><span class="sxs-lookup"><span data-stu-id="93e0c-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="93e0c-156">Os processos subjacentes podem ter sido deixados em execução e a limpeza pode ser necessária para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="93e0c-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="93e0c-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exceção** (10)</span><span class="sxs-lookup"><span data-stu-id="93e0c-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-158">O trabalho está em um estado anormal que pode indicar uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="93e0c-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="93e0c-159">O status real pode ser exibido, embora objetos específicos do trabalho.</span><span class="sxs-lookup"><span data-stu-id="93e0c-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="93e0c-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (11)</span><span class="sxs-lookup"><span data-stu-id="93e0c-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-161">O trabalho está em um estado específico de fornecedor que dá suporte à descoberta de problemas, ou resolução, ou ambos</span><span class="sxs-lookup"><span data-stu-id="93e0c-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="93e0c-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Consulta pendente** (12)</span><span class="sxs-lookup"><span data-stu-id="93e0c-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="93e0c-163">Aguardando um cliente resolver uma consulta.</span><span class="sxs-lookup"><span data-stu-id="93e0c-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="93e0c-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (13.. 32767)</span><span class="sxs-lookup"><span data-stu-id="93e0c-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="93e0c-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="93e0c-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93e0c-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="93e0c-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93e0c-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93e0c-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93e0c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-169">Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome")</span><span class="sxs-lookup"><span data-stu-id="93e0c-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="93e0c-170">O nome amigável da instância do.</span><span class="sxs-lookup"><span data-stu-id="93e0c-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="93e0c-171">Além disso, o nome amigável do usuário pode ser usado como uma propriedade para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="93e0c-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="93e0c-172">O nome não precisa ser exclusivo no namespace.</span><span class="sxs-lookup"><span data-stu-id="93e0c-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="93e0c-173">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="93e0c-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93e0c-174">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93e0c-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="93e0c-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-176">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93e0c-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93e0c-177">Indica por quanto tempo um trabalho concluído é retido.</span><span class="sxs-lookup"><span data-stu-id="93e0c-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="93e0c-178">O valor padrão é "00000000000500.000000:000" (cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="93e0c-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="93e0c-179">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="93e0c-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93e0c-180">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93e0c-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93e0c-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93e0c-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93e0c-182">A data ou a hora em que o estado do trabalho foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="93e0c-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="93e0c-183">Se o estado do trabalho não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de zero.</span><span class="sxs-lookup"><span data-stu-id="93e0c-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93e0c-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e0c-184">Requirements</span></span>



| <span data-ttu-id="93e0c-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e0c-185">Requirement</span></span> | <span data-ttu-id="93e0c-186">Valor</span><span class="sxs-lookup"><span data-stu-id="93e0c-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e0c-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e0c-187">Minimum supported client</span></span><br/> | <span data-ttu-id="93e0c-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="93e0c-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="93e0c-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e0c-189">Minimum supported server</span></span><br/> | <span data-ttu-id="93e0c-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93e0c-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="93e0c-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="93e0c-191">Namespace</span></span><br/>                | <span data-ttu-id="93e0c-192">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="93e0c-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93e0c-193">MOF</span><span class="sxs-lookup"><span data-stu-id="93e0c-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93e0c-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93e0c-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93e0c-195">DLL</span><span class="sxs-lookup"><span data-stu-id="93e0c-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e0c-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93e0c-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93e0c-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="93e0c-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e0c-198">**Trabalho do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="93e0c-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

