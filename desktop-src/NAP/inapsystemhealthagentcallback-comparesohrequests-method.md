---
title: Método INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: É usado pelo SHA para comparar solicitações SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Método CompareSoHRequests NAP
- Método CompareSoHRequests NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789633"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="78a56-106">Método INapSystemHealthAgentCallback:: CompareSoHRequests</span><span class="sxs-lookup"><span data-stu-id="78a56-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="78a56-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="78a56-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="78a56-108">O método **INapSystemHealthAgentCallback:: CompareSoHRequests** é usado pelo Sha para comparar as solicitações soh.</span><span class="sxs-lookup"><span data-stu-id="78a56-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a56-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78a56-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="78a56-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78a56-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78a56-111">*LHS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78a56-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a56-112">Um ponteiro para o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à esquerda da operação de comparação.</span><span class="sxs-lookup"><span data-stu-id="78a56-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="78a56-113">*RHS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78a56-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a56-114">Um ponteiro para o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à direita da operação de comparação.</span><span class="sxs-lookup"><span data-stu-id="78a56-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="78a56-115">*IsEqual* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="78a56-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78a56-116">Um ponteiro para um **bool** que é **verdadeiro** se *LHS* e *RHS* são semanticamente iguais e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="78a56-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78a56-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78a56-117">Return value</span></span>

<span data-ttu-id="78a56-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="78a56-118">This method can return one of these values.</span></span>



| <span data-ttu-id="78a56-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="78a56-119">Return code</span></span>                                                                               | <span data-ttu-id="78a56-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="78a56-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="78a56-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78a56-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="78a56-122">Indica êxito.</span><span class="sxs-lookup"><span data-stu-id="78a56-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="78a56-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="78a56-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="78a56-124">O método não foi implementado pelo SHA.</span><span class="sxs-lookup"><span data-stu-id="78a56-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78a56-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="78a56-125">Remarks</span></span>

<span data-ttu-id="78a56-126">Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.</span><span class="sxs-lookup"><span data-stu-id="78a56-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="78a56-127">O SHA deve comparar o SoHs e retornar **true** se SoHs for semanticamente igual.</span><span class="sxs-lookup"><span data-stu-id="78a56-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="78a56-128">O NapAgent usa essas informações para determinar se uma troca de SoH deve ser iniciada devido à alteração do estado do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="78a56-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="78a56-129">Se os SHAs tiverem colocado IDs incrementais ou carimbos de data/hora em sua SoH, SoHs poderá ser semanticamente igual (ou seja, eles podem transmitir as mesmas informações de integridade), mas podem ser desiguais por byte.</span><span class="sxs-lookup"><span data-stu-id="78a56-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="78a56-130">Os SHAs devem implementar essa função para verificar a igualdade semântica de SoHs.</span><span class="sxs-lookup"><span data-stu-id="78a56-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="78a56-131">Se os SHAs não tiverem colocado carimbos de data/hora ou IDs em seus SoHs, eles poderão optar por não implementar essa função e retornar e **\_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="78a56-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="78a56-132">Nesse caso, o NapAgent executa uma comparação de byte no [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="78a56-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="78a56-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a56-133">Requirements</span></span>



| <span data-ttu-id="78a56-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a56-134">Requirement</span></span> | <span data-ttu-id="78a56-135">Valor</span><span class="sxs-lookup"><span data-stu-id="78a56-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a56-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78a56-136">Minimum supported client</span></span><br/> | <span data-ttu-id="78a56-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78a56-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78a56-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78a56-138">Minimum supported server</span></span><br/> | <span data-ttu-id="78a56-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78a56-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78a56-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78a56-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="78a56-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="78a56-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="78a56-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="78a56-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78a56-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78a56-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a56-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="78a56-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a56-145">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="78a56-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="78a56-146">**SoH**</span><span class="sxs-lookup"><span data-stu-id="78a56-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





