---
title: Método SyncNamingContext da classe MSAD_ReplNeighbor
description: Chama a função DsReplicaSync que sincroniza um contexto de nomenclatura de destino com uma de suas origens.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory do método SyncNamingContext
- Método SyncNamingContext Active Directory, classe MSAD_ReplNeighbor
- Classe MSAD_ReplNeighbor Active Directory, método SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455669"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a><span data-ttu-id="9da69-106">Método SyncNamingContext da \_ classe REPLNEIGHBOR MSAD</span><span class="sxs-lookup"><span data-stu-id="9da69-106">SyncNamingContext method of the MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="9da69-107">Chama a função [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) que sincroniza um contexto de nomenclatura de destino com uma de suas origens.</span><span class="sxs-lookup"><span data-stu-id="9da69-107">Calls the [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) function that synchronizes a destination naming context with one of its sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da69-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9da69-108">Syntax</span></span>


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a><span data-ttu-id="9da69-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9da69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da69-110">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9da69-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9da69-111">Dados adicionais que determinam como o método processa a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9da69-111">Additional data that determines how the method processes the request.</span></span> <span data-ttu-id="9da69-112">Esse parâmetro pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9da69-112">This parameter can be a combination of the following values.</span></span>

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span data-ttu-id="9da69-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Adicionar referência de REPSYNC DS \_**</span><span class="sxs-lookup"><span data-stu-id="9da69-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS\_REPSYNC\_ADD\_REFERENCE**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-114">Faz com que o DSA (Directory System Agent de origem) Verifique se o DSA local está presente na lista replicações de origem para.</span><span class="sxs-lookup"><span data-stu-id="9da69-114">Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list.</span></span> <span data-ttu-id="9da69-115">Se o DSA local não estiver presente, ele será adicionado.</span><span class="sxs-lookup"><span data-stu-id="9da69-115">If the local DSA is not present, it is added.</span></span> <span data-ttu-id="9da69-116">Isso garante que a origem envie notificações de alteração.</span><span class="sxs-lookup"><span data-stu-id="9da69-116">This ensures that the source sends change notifications.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span data-ttu-id="9da69-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ todas as \_ fontes**</span><span class="sxs-lookup"><span data-stu-id="9da69-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS\_REPSYNC\_ALL\_SOURCES**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-118">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="9da69-118">This value is not supported.</span></span>

<span data-ttu-id="9da69-119">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Sincroniza de todas as fontes.</span><span class="sxs-lookup"><span data-stu-id="9da69-119">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Synchronizes from all sources.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span data-ttu-id="9da69-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ operação assíncrona de REPSYNC DS \_**</span><span class="sxs-lookup"><span data-stu-id="9da69-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS\_REPSYNC\_ASYNCHRONOUS\_OPERATION**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-121">Executa essa operação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9da69-121">Performs this operation asynchronously.</span></span>

<span data-ttu-id="9da69-122">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Necessário ao usar **DS \_ REPSYNC \_ todas as \_ fontes**.</span><span class="sxs-lookup"><span data-stu-id="9da69-122">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Required when using **DS\_REPSYNC\_ALL\_SOURCES**.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span data-ttu-id="9da69-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_força de REPSYNC DS \_**</span><span class="sxs-lookup"><span data-stu-id="9da69-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS\_REPSYNC\_FORCE**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-124">Sincroniza mesmo que o link esteja desabilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="9da69-124">Synchronizes even if the link is currently disabled.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span data-ttu-id="9da69-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ completo**</span><span class="sxs-lookup"><span data-stu-id="9da69-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS\_REPSYNC\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-126">Sincroniza a partir do primeiro número de sequência de atualização (USN).</span><span class="sxs-lookup"><span data-stu-id="9da69-126">Synchronizes starting from the first Update Sequence Number (USN).</span></span>

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span data-ttu-id="9da69-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_sistema de \_ mensagens entre sites REPSYNC DS \_**</span><span class="sxs-lookup"><span data-stu-id="9da69-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS\_REPSYNC\_INTERSITE\_MESSAGING**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-128">Sincroniza usando um ISM.</span><span class="sxs-lookup"><span data-stu-id="9da69-128">Synchronizes using an ISM.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span data-ttu-id="9da69-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**\_REPSYNC DS \_ sem \_ descarte**</span><span class="sxs-lookup"><span data-stu-id="9da69-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS\_REPSYNC\_NO\_DISCARD**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-130">Não descarta essa solicitação de sincronização, mesmo que uma sincronização semelhante esteja pendente.</span><span class="sxs-lookup"><span data-stu-id="9da69-130">Does not discard this synchronization request, even if a similar synchronization is pending.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span data-ttu-id="9da69-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ periódico**</span><span class="sxs-lookup"><span data-stu-id="9da69-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS\_REPSYNC\_PERIODIC**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-132">Indica que esta operação é uma solicitação de sincronização periódica agendada pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="9da69-132">Indicates that this operation is a periodic synchronization request that is scheduled by the administrator.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span data-ttu-id="9da69-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ urgente**</span><span class="sxs-lookup"><span data-stu-id="9da69-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS\_REPSYNC\_URGENT**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-134">Indica que esta operação é uma notificação de uma atualização que está marcada como urgente.</span><span class="sxs-lookup"><span data-stu-id="9da69-134">Indicates that this operation is a notification of an update that is marked as urgent.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span data-ttu-id="9da69-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ gravável**</span><span class="sxs-lookup"><span data-stu-id="9da69-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS\_REPSYNC\_WRITEABLE**</span></span>


</dt> <dd>

<span data-ttu-id="9da69-136">Indica que esta réplica é gravável.</span><span class="sxs-lookup"><span data-stu-id="9da69-136">Indicates that this replica is writable.</span></span> <span data-ttu-id="9da69-137">Se esse sinalizador não for definido, a réplica será somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9da69-137">If this flag is not set, the replica is read-only.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da69-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9da69-138">Return value</span></span>

<span data-ttu-id="9da69-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9da69-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da69-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9da69-140">Requirements</span></span>



| <span data-ttu-id="9da69-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9da69-141">Requirement</span></span> | <span data-ttu-id="9da69-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9da69-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9da69-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9da69-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9da69-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9da69-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9da69-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9da69-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9da69-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9da69-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9da69-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="9da69-147">Namespace</span></span><br/>                | <span data-ttu-id="9da69-148">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="9da69-148">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="9da69-149">MOF</span><span class="sxs-lookup"><span data-stu-id="9da69-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9da69-150"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9da69-150"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="9da69-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9da69-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9da69-152"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9da69-152"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da69-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9da69-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da69-154">**MSAD \_ ReplNeighbor**</span><span class="sxs-lookup"><span data-stu-id="9da69-154">**MSAD\_ReplNeighbor**</span></span>](msad-replneighbor.md)
</dt> </dl>

 

 





