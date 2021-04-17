---
description: O método GetPhoneNumbers Obtém uma matriz de números de telefone associados a um blob de conferência.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'Método ITSdp:: GetPhoneNumbers (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783365"
---
# <a name="itsdpgetphonenumbers-method"></a><span data-ttu-id="6dc70-103">Método ITSdp:: GetPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="6dc70-103">ITSdp::GetPhoneNumbers method</span></span>

<span data-ttu-id="6dc70-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6dc70-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6dc70-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6dc70-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6dc70-106">O método **GetPhoneNumbers** Obtém uma matriz de números de telefone associados a um blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="6dc70-106">The **GetPhoneNumbers** method gets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc70-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dc70-107">Syntax</span></span>


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="6dc70-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dc70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dc70-109">*pNumbers* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dc70-109">*pNumbers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc70-110">Ponteiro de **variante** para um SafeArray dos números de telefone de listagem de **BSTRs**.</span><span class="sxs-lookup"><span data-stu-id="6dc70-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="6dc70-111">*pNames* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dc70-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc70-112">Ponteiro de **variante** para um SafeArray de nomes de listagem **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="6dc70-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dc70-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dc70-113">Return value</span></span>

<span data-ttu-id="6dc70-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6dc70-114">This method can return one of these values.</span></span>



| <span data-ttu-id="6dc70-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6dc70-115">Return code</span></span>                                                                                   | <span data-ttu-id="6dc70-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6dc70-116">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6dc70-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6dc70-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6dc70-118">Method succeeded.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6dc70-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6dc70-120">O parâmetro *pNumbers* ou *pNames* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="6dc70-120">The *pNumbers* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="6dc70-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6dc70-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="6dc70-122">Insufficient memory exists to perform the operation.</span></span><br/>         |
| <dl> <span data-ttu-id="6dc70-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6dc70-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6dc70-124">Unspecified error.</span></span><br/>                                           |
| <dl> <span data-ttu-id="6dc70-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6dc70-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="6dc70-126">This method is not yet implemented.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="6dc70-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dc70-127">Remarks</span></span>

<span data-ttu-id="6dc70-128">As listas das quais *pNumbers* e *pNames* apontam têm o mesmo comprimento.</span><span class="sxs-lookup"><span data-stu-id="6dc70-128">The lists that *pNumbers* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc70-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dc70-129">Requirements</span></span>



| <span data-ttu-id="6dc70-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dc70-130">Requirement</span></span> | <span data-ttu-id="6dc70-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6dc70-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc70-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6dc70-132">TAPI version</span></span><br/> | <span data-ttu-id="6dc70-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6dc70-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6dc70-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dc70-134">Header</span></span><br/>       | <dl> <span data-ttu-id="6dc70-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dc70-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6dc70-136">Library</span></span><br/>      | <dl> <span data-ttu-id="6dc70-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6dc70-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6dc70-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="6dc70-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dc70-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc70-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dc70-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc70-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="6dc70-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




