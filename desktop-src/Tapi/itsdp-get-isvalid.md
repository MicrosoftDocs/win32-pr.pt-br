---
description: O \_ método Get IsValid valida o protocolo SDP (Session Descriptor Protocol), consulte o blob RFC 2327) para a estrutura e os valores de campo.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Método ITSdp:: get_IsValid (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756994"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="1c0ad-103">Método IsValid de ITSdp:: get \_</span><span class="sxs-lookup"><span data-stu-id="1c0ad-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="1c0ad-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c0ad-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1c0ad-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1c0ad-106">O método **Get \_ IsValid** valida o protocolo SDP (Session Descriptor Protocol), consulte o blob RFC 2327) para a estrutura e os valores de campo.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0ad-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c0ad-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="1c0ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c0ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c0ad-109">*pfIsValid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1c0ad-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c0ad-110">Indica se a estrutura do blob é válida.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c0ad-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c0ad-111">Return value</span></span>

<span data-ttu-id="1c0ad-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1c0ad-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1c0ad-113">Return code</span></span>                                                                                   | <span data-ttu-id="1c0ad-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c0ad-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1c0ad-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1c0ad-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1c0ad-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1c0ad-118">O parâmetro *pfIsValid* não é válido.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="1c0ad-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1c0ad-120">O parâmetro *pfIsValid* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="1c0ad-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1c0ad-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1c0ad-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1c0ad-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1c0ad-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1c0ad-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="1c0ad-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c0ad-127">Requirements</span></span>



| <span data-ttu-id="1c0ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c0ad-128">Requirement</span></span> | <span data-ttu-id="1c0ad-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1c0ad-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0ad-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1c0ad-130">TAPI version</span></span><br/> | <span data-ttu-id="1c0ad-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1c0ad-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1c0ad-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c0ad-132">Header</span></span><br/>       | <dl> <span data-ttu-id="1c0ad-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c0ad-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c0ad-134">Library</span></span><br/>      | <dl> <span data-ttu-id="1c0ad-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1c0ad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1c0ad-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="1c0ad-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0ad-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c0ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0ad-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="1c0ad-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




