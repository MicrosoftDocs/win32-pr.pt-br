---
title: Método ExecuteKCC da classe MSAD_DomainController
description: Chama a função DsReplicaConsistencyCheck, que invoca a Knowledge Consistency Checker (KCC) para verificar a topologia de replicação.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory do método ExecuteKCC
- Método ExecuteKCC Active Directory, classe MSAD_DomainController
- Classe MSAD_DomainController Active Directory, método ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753875"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="4290e-106">Método ExecuteKCC da \_ classe DOMAINCONTROLLER MSAD</span><span class="sxs-lookup"><span data-stu-id="4290e-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="4290e-107">Chama a função [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , que invoca a Knowledge CONSISTENCY Checker (KCC) para verificar a topologia de replicação.</span><span class="sxs-lookup"><span data-stu-id="4290e-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="4290e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4290e-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4290e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4290e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4290e-110">*TaskId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4290e-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4290e-111">A tarefa que o KCC deve executar.</span><span class="sxs-lookup"><span data-stu-id="4290e-111">The task that the KCC should execute.</span></span> <span data-ttu-id="4290e-112">**DS \_ A \_ topologia de \_ atualização \_ de TaskId do KCC** é o único valor com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="4290e-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="4290e-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4290e-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4290e-114">Um conjunto de sinalizadores que modificam o comportamento do método **ExecuteKCC** .</span><span class="sxs-lookup"><span data-stu-id="4290e-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="4290e-115">Esse parâmetro pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4290e-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="4290e-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**\_ \_ \_ operação assíncrona de sinalizador do KCC do DS \_**</span><span class="sxs-lookup"><span data-stu-id="4290e-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="4290e-117">A tarefa é enfileirada e, em seguida, a função retorna sem aguardar a conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4290e-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="4290e-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**sinalizador do KCC do DS \_ \_ \_ úmido**</span><span class="sxs-lookup"><span data-stu-id="4290e-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="4290e-119">A tarefa não será adicionada à fila se outra tarefa em fila for executada em breve.</span><span class="sxs-lookup"><span data-stu-id="4290e-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4290e-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4290e-120">Return value</span></span>

<span data-ttu-id="4290e-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4290e-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4290e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4290e-122">Requirements</span></span>



| <span data-ttu-id="4290e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4290e-123">Requirement</span></span> | <span data-ttu-id="4290e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4290e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4290e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4290e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4290e-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4290e-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4290e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4290e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4290e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4290e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4290e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4290e-129">Namespace</span></span><br/>                | <span data-ttu-id="4290e-130">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="4290e-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="4290e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4290e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4290e-132"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4290e-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="4290e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4290e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4290e-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4290e-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4290e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4290e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4290e-136">**MSAD \_ DomainController**</span><span class="sxs-lookup"><span data-stu-id="4290e-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 





