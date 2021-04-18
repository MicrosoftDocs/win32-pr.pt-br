---
description: O método getemailnames Obtém uma matriz de nomes de email associados ao blob de conferência.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'Método ITSdp:: getemailnames (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784089"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="c695d-103">Método ITSdp:: getemailnames</span><span class="sxs-lookup"><span data-stu-id="c695d-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="c695d-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c695d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c695d-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c695d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c695d-106">O método **Getemailnames** Obtém uma matriz de nomes de email associados ao blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="c695d-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="c695d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c695d-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="c695d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c695d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c695d-109">*pAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c695d-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c695d-110">Ponteiro de **variante** para um SafeArray de **BSTR** s listando endereços de email.</span><span class="sxs-lookup"><span data-stu-id="c695d-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="c695d-111">*pNames* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c695d-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c695d-112">Ponteiro de **variante** para um SafeArray de nomes de listagem **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="c695d-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c695d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c695d-113">Return value</span></span>

<span data-ttu-id="c695d-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c695d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c695d-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c695d-115">Return code</span></span>                                                                                   | <span data-ttu-id="c695d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c695d-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c695d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c695d-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c695d-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="c695d-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c695d-120">O parâmetro *pAddresses* ou *pNames* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="c695d-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="c695d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c695d-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c695d-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="c695d-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c695d-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c695d-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="c695d-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c695d-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="c695d-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c695d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c695d-127">Remarks</span></span>

<span data-ttu-id="c695d-128">As listas das quais *pAddresses* e *pNames* apontam têm o mesmo comprimento.</span><span class="sxs-lookup"><span data-stu-id="c695d-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="c695d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c695d-129">Requirements</span></span>



| <span data-ttu-id="c695d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c695d-130">Requirement</span></span> | <span data-ttu-id="c695d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c695d-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c695d-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c695d-132">TAPI version</span></span><br/> | <span data-ttu-id="c695d-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c695d-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c695d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c695d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c695d-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c695d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c695d-136">Library</span></span><br/>      | <dl> <span data-ttu-id="c695d-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c695d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c695d-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="c695d-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c695d-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c695d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c695d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c695d-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="c695d-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




