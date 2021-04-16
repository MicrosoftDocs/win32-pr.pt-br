---
title: Método INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: Assina um servidor de certificado de integridade (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Método SubscribeCertByGroup NAP
- Método SubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, método SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751172"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="9170e-106">Método INapCertRelyingParty:: SubscribeCertByGroup</span><span class="sxs-lookup"><span data-stu-id="9170e-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="9170e-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="9170e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9170e-108">O método **SubscribeCertByGroup** assina um servidor de certificado de integridade (HCS).</span><span class="sxs-lookup"><span data-stu-id="9170e-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="9170e-109">O HCS já deve estar registrado antes da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9170e-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9170e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9170e-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="9170e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9170e-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="9170e-112">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="9170e-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9170e-113">Um [**EnforcementEntityId**](nap-datatypes.md) que contém a ID do cliente de imposição que está se inscrevendo.</span><span class="sxs-lookup"><span data-stu-id="9170e-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="9170e-114">*SubscriberName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9170e-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9170e-115">O nome do assinante.</span><span class="sxs-lookup"><span data-stu-id="9170e-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="9170e-116">Atualmente, isso é usado apenas para fins de log.</span><span class="sxs-lookup"><span data-stu-id="9170e-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="9170e-117">*reservado* \[ para no\]</span><span class="sxs-lookup"><span data-stu-id="9170e-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9170e-118">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9170e-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9170e-119">*certExists* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9170e-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9170e-120">Indica se um certificado de integridade deste HCS já está sendo mantido pelo NapAgent e está presente no repositório de computadores.</span><span class="sxs-lookup"><span data-stu-id="9170e-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="9170e-121">Se for **true**, um certificado de integridade já estará sendo mantido e estará presente.</span><span class="sxs-lookup"><span data-stu-id="9170e-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="9170e-122">Se for **false**, um certificado de integridade não estará sendo mantido e estará presente no momento.</span><span class="sxs-lookup"><span data-stu-id="9170e-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9170e-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9170e-123">Return value</span></span>

<span data-ttu-id="9170e-124">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="9170e-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="9170e-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9170e-125">Return code</span></span>                                                                                     | <span data-ttu-id="9170e-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="9170e-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9170e-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9170e-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9170e-128">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="9170e-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="9170e-129"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9170e-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9170e-130">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="9170e-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9170e-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9170e-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9170e-132">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="9170e-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9170e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9170e-133">Requirements</span></span>



| <span data-ttu-id="9170e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9170e-134">Requirement</span></span> | <span data-ttu-id="9170e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="9170e-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9170e-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9170e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9170e-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9170e-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9170e-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9170e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9170e-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9170e-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9170e-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9170e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9170e-141"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="9170e-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="9170e-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="9170e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9170e-143"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9170e-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9170e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9170e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9170e-145">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="9170e-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





