---
description: O \_ método Get NumAddresses Obtém o número de endereços a serem usados para a sessão.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Método ITConnection:: get_NumAddresses (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811928"
---
# <a name="itconnectionget_numaddresses-method"></a><span data-ttu-id="7fa9b-103">Método ITConnection:: get \_ NumAddresses</span><span class="sxs-lookup"><span data-stu-id="7fa9b-103">ITConnection::get\_NumAddresses method</span></span>

<span data-ttu-id="7fa9b-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7fa9b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="7fa9b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7fa9b-106">O método **Get \_ NumAddresses** Obtém o número de endereços a serem usados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-106">The **get\_NumAddresses** method gets the number of addresses to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa9b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fa9b-107">Syntax</span></span>


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="7fa9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fa9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa9b-109">*pNumAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7fa9b-109">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa9b-110">Número de endereços para a sessão.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-110">Number of addresses for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa9b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fa9b-111">Return value</span></span>

<span data-ttu-id="7fa9b-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7fa9b-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7fa9b-113">Return code</span></span>                                                                                   | <span data-ttu-id="7fa9b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fa9b-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fa9b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7fa9b-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7fa9b-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7fa9b-118">O parâmetro *pNumAddresse* s não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-118">The *pNumAddresse* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="7fa9b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7fa9b-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="7fa9b-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7fa9b-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7fa9b-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7fa9b-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="7fa9b-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="7fa9b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa9b-125">Requirements</span></span>



| <span data-ttu-id="7fa9b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa9b-126">Requirement</span></span> | <span data-ttu-id="7fa9b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa9b-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa9b-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="7fa9b-128">TAPI version</span></span><br/> | <span data-ttu-id="7fa9b-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7fa9b-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7fa9b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fa9b-130">Header</span></span><br/>       | <dl> <span data-ttu-id="7fa9b-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fa9b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fa9b-132">Library</span></span><br/>      | <dl> <span data-ttu-id="7fa9b-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7fa9b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7fa9b-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="7fa9b-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fa9b-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa9b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fa9b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa9b-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="7fa9b-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




