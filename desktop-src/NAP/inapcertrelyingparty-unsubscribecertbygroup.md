---
title: Método INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Cancela a assinatura de um servidor de certificado de integridade (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Método UnSubscribeCertByGroup NAP
- Método UnSubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, método UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918591"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="24414-106">Método INapCertRelyingParty:: UnSubscribeCertByGroup</span><span class="sxs-lookup"><span data-stu-id="24414-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="24414-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="24414-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="24414-108">O método **UnSubscribeCertByGroup** cancela a assinatura de um servidor de certificado de integridade (HCS).</span><span class="sxs-lookup"><span data-stu-id="24414-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="24414-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24414-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="24414-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24414-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="24414-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="24414-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24414-112">Um [**EnforcementEntityId**](nap-datatypes.md) que contém a ID do cliente de imposição que está sendo cancelado.</span><span class="sxs-lookup"><span data-stu-id="24414-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="24414-113">*reservado* \[ para no\]</span><span class="sxs-lookup"><span data-stu-id="24414-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24414-114">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="24414-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24414-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24414-115">Return value</span></span>

<span data-ttu-id="24414-116">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="24414-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="24414-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="24414-117">Return code</span></span>                                                                                     | <span data-ttu-id="24414-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="24414-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="24414-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24414-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="24414-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="24414-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="24414-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="24414-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="24414-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="24414-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="24414-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="24414-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="24414-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="24414-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24414-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="24414-125">Remarks</span></span>

<span data-ttu-id="24414-126">Se não houver nenhum outro assinante para o HCS, o NapAgent excluirá os certificados de integridade correspondentes do repositório do computador local.</span><span class="sxs-lookup"><span data-stu-id="24414-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="24414-127">Antes de chamar esse método, chame [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span><span class="sxs-lookup"><span data-stu-id="24414-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24414-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24414-128">Requirements</span></span>



| <span data-ttu-id="24414-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="24414-129">Requirement</span></span> | <span data-ttu-id="24414-130">Valor</span><span class="sxs-lookup"><span data-stu-id="24414-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24414-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24414-131">Minimum supported client</span></span><br/> | <span data-ttu-id="24414-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24414-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24414-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24414-133">Minimum supported server</span></span><br/> | <span data-ttu-id="24414-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24414-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="24414-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24414-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="24414-136"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="24414-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="24414-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="24414-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24414-138"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="24414-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24414-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="24414-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24414-140">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="24414-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





