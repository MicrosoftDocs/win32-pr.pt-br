---
title: Classe MSAD_ReplPendingOp
description: Representa a \_ estrutura de op de repl DS \_ , que descreve uma tarefa de replicação que está atualmente em execução ou com execução pendente.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_ReplPendingOp Active Directory
- Active Directory de MSAD_ReplPendingOp classe, descrita
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369627"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="4c8fe-105">\_Classe MSAD ReplPendingOp</span><span class="sxs-lookup"><span data-stu-id="4c8fe-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="4c8fe-106">Representa a estrutura de [**\_ \_ op de repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , que descreve uma tarefa de replicação que está atualmente em execução ou com execução pendente.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="4c8fe-107">Essa estrutura é retornada pela função [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="4c8fe-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8fe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c8fe-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="4c8fe-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4c8fe-109">Members</span></span>

<span data-ttu-id="4c8fe-110">A classe **MSAD \_ ReplPendingOp** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c8fe-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="4c8fe-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c8fe-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c8fe-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c8fe-112">Properties</span></span>

<span data-ttu-id="4c8fe-113">A classe **MSAD \_ ReplPendingOp** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c8fe-114">**DsaAddress**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-117">Obtém o endereço de rede específico de transporte do servidor remoto que está associado a esta operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="4c8fe-118">**NULL** se não houver um servidor remoto associado a esta operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-119">**DsaDN**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-122">Obtém o caminho X. 500 do DSA associado ao servidor remoto que corresponde a essa operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="4c8fe-123">**NULL** se nenhum servidor remoto corresponder a esta operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-124">**DsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-127">Obtém o valor do atributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) do DSA que é identificado pela propriedade **DsaDN** .</span><span class="sxs-lookup"><span data-stu-id="4c8fe-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-128">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-131">Obtém o caminho X. 500 do NC (contexto de nomenclatura) que está associado a esta operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-132">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-135">Obtém o atributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) do NC que é identificado pela propriedade **NamingContextDN** .</span><span class="sxs-lookup"><span data-stu-id="4c8fe-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-136">**OpStartTime**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-137">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-139">Obtém a hora em que a operação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="4c8fe-140">**NULL** se essa operação ainda estiver na fila.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-141">**Opções**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-144">Obtém o conjunto de sinalizadores que fornece dados adicionais sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="4c8fe-145">O conteúdo desse membro é determinado pelo valor da propriedade **OpType** .</span><span class="sxs-lookup"><span data-stu-id="4c8fe-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="4c8fe-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_sincronização de \_ tipo de op DS repl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="4c8fe-147">Contém zero ou uma combinação de um ou mais dos \**DS \_ \_ \* REPSYNC* _ valores, conforme definido para o parâmetro _Options \* em [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span><span class="sxs-lookup"><span data-stu-id="4c8fe-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="4c8fe-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_ \_ \_ Adicionar tipo de op \_ do DS repl**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="4c8fe-149">Contém zero ou uma combinação de um ou mais dos \**DS \_ \_ \* REPADD* _ valores, conforme definido para o parâmetro _Options \* em [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span><span class="sxs-lookup"><span data-stu-id="4c8fe-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="4c8fe-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_exclusão do \_ tipo de op DS repl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="4c8fe-151">Contém zero ou uma combinação de um ou mais dos \**DS \_ \_ \* REPDEL* _ valores, conforme definido para o parâmetro _Options \* em [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span><span class="sxs-lookup"><span data-stu-id="4c8fe-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="4c8fe-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**\_modificação de \_ tipo de op \_ \_ do DS repl**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="4c8fe-153">Contém zero ou uma combinação de um ou mais dos \**DS \_ \_ \* REPMOD* _ valores, conforme definido para o parâmetro _Options \* em [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span><span class="sxs-lookup"><span data-stu-id="4c8fe-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="4c8fe-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_referências de \_ atualização do tipo de op DS repl \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="4c8fe-155">Contém zero ou uma combinação de um ou mais dos \**DS \_ \_ \* REPSUPD* _ valores, conforme definido para o parâmetro _Options \* em [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span><span class="sxs-lookup"><span data-stu-id="4c8fe-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4c8fe-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-159">Obtém o valor do [**\_ tipo de \_ op \_ DS repl**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) que indica o tipo de operação que essa classe representa.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-160">**PositionInQ**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-163">Obtém a posição desta operação na fila.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-164">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-167">Obtém a prioridade desta operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-167">Gets the priority of this operation.</span></span> <span data-ttu-id="4c8fe-168">As tarefas de prioridade mais alta são executadas primeiro.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="4c8fe-169">A prioridade é calculada pelo servidor com base no tipo de operação que essa classe representa e nos parâmetros da operação.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-170">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-173">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c8fe-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-174">Obtém a ID da operação, que é exclusiva por máquina e por inicialização.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="4c8fe-175">**Enfileirado**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c8fe-176">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4c8fe-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4c8fe-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c8fe-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c8fe-178">Obtém a hora em que essa operação foi adicionada à fila.</span><span class="sxs-lookup"><span data-stu-id="4c8fe-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c8fe-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c8fe-179">Requirements</span></span>



| <span data-ttu-id="4c8fe-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8fe-180">Requirement</span></span> | <span data-ttu-id="4c8fe-181">Valor</span><span class="sxs-lookup"><span data-stu-id="4c8fe-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8fe-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c8fe-182">Minimum supported client</span></span><br/> | <span data-ttu-id="4c8fe-183">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c8fe-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4c8fe-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c8fe-184">Minimum supported server</span></span><br/> | <span data-ttu-id="4c8fe-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c8fe-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c8fe-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c8fe-186">Namespace</span></span><br/>                | <span data-ttu-id="4c8fe-187">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="4c8fe-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="4c8fe-188">MOF</span><span class="sxs-lookup"><span data-stu-id="4c8fe-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c8fe-189"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c8fe-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c8fe-190">DLL</span><span class="sxs-lookup"><span data-stu-id="4c8fe-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c8fe-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c8fe-191"><dt>Replprov.dll</dt></span></span> </dl> |



 

