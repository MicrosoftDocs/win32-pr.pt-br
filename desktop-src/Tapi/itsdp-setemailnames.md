---
description: O método setemailnames define uma matriz de endereços de email associados ao blob de conferência.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'Método ITSdp:: setemailnames (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761960"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="402de-103">Método ITSdp:: setemailnames</span><span class="sxs-lookup"><span data-stu-id="402de-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="402de-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="402de-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="402de-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="402de-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="402de-106">O método **Setemailnames** define uma matriz de endereços de email associados ao blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="402de-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="402de-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="402de-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="402de-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="402de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="402de-109">*Endereços* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="402de-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402de-110">SAFEARRAY de **BSTR** s listando endereços de email.</span><span class="sxs-lookup"><span data-stu-id="402de-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="402de-111">*Nomes* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="402de-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402de-112">SAFEARRAY de nomes de listagem **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="402de-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="402de-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="402de-113">Return value</span></span>

<span data-ttu-id="402de-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="402de-114">This method can return one of these values.</span></span>



| <span data-ttu-id="402de-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="402de-115">Return code</span></span>                                                                                   | <span data-ttu-id="402de-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="402de-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="402de-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="402de-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="402de-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="402de-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="402de-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="402de-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="402de-120">O parâmetro *Addresses* ou *Names* não é válido.</span><span class="sxs-lookup"><span data-stu-id="402de-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="402de-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="402de-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="402de-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="402de-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="402de-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="402de-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="402de-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="402de-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="402de-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="402de-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="402de-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="402de-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="402de-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="402de-127">Remarks</span></span>

<span data-ttu-id="402de-128">As listas que os *endereços* e os *nomes* apontam têm o mesmo comprimento.</span><span class="sxs-lookup"><span data-stu-id="402de-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="402de-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="402de-129">Requirements</span></span>



| <span data-ttu-id="402de-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="402de-130">Requirement</span></span> | <span data-ttu-id="402de-131">Valor</span><span class="sxs-lookup"><span data-stu-id="402de-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="402de-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="402de-132">TAPI version</span></span><br/> | <span data-ttu-id="402de-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="402de-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="402de-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="402de-134">Header</span></span><br/>       | <dl> <span data-ttu-id="402de-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="402de-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="402de-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="402de-136">Library</span></span><br/>      | <dl> <span data-ttu-id="402de-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="402de-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="402de-138">DLL</span><span class="sxs-lookup"><span data-stu-id="402de-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="402de-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="402de-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="402de-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="402de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="402de-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="402de-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




