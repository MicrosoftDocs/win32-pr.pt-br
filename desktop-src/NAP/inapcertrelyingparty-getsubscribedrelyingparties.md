---
title: Método INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Obtém uma lista de terceiras partes confiáveis que se inscreveram.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Método GetSubscribedRelyingParties NAP
- Método GetSubscribedRelyingParties NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, método GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454737"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="3310b-106">Método INapCertRelyingParty:: GetSubscribedRelyingParties</span><span class="sxs-lookup"><span data-stu-id="3310b-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="3310b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="3310b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3310b-108">O método **GetSubscribedRelyingParties** Obtém uma lista de terceiras partes confiáveis que se inscreveram.</span><span class="sxs-lookup"><span data-stu-id="3310b-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3310b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3310b-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="3310b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3310b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3310b-111">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="3310b-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3310b-112">Um ponteiro para um [**EnforcementEntityCount**](nap-datatypes.md) que contém o número de terceiras partes confiáveis assinadas.</span><span class="sxs-lookup"><span data-stu-id="3310b-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="3310b-113">*relyingParties* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3310b-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3310b-114">Um ponteiro para um ponteiro para um [**EnforcementEntityId**](nap-datatypes.md) que contém a lista de terceiras partes confiáveis inscritas.</span><span class="sxs-lookup"><span data-stu-id="3310b-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3310b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3310b-115">Return value</span></span>

<span data-ttu-id="3310b-116">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="3310b-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="3310b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3310b-117">Return code</span></span>                                                                                     | <span data-ttu-id="3310b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3310b-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3310b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3310b-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3310b-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="3310b-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="3310b-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3310b-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3310b-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3310b-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3310b-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3310b-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3310b-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="3310b-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3310b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3310b-125">Remarks</span></span>

<span data-ttu-id="3310b-126">O chamador deve liberar o parâmetro *relyingParties* usando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="3310b-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3310b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3310b-127">Requirements</span></span>



| <span data-ttu-id="3310b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3310b-128">Requirement</span></span> | <span data-ttu-id="3310b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3310b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3310b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3310b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3310b-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3310b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3310b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3310b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3310b-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3310b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3310b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3310b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3310b-135"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="3310b-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="3310b-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="3310b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3310b-137"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3310b-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3310b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3310b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3310b-139">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="3310b-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





