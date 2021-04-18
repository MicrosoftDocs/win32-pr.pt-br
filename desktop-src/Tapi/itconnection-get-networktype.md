---
description: O \_ método Get NetworkType Obtém o tipo de rede.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Método ITConnection:: get_NetworkType (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31189ec0e3b42e3ed249cd0c62365b1f8c793908
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792626"
---
# <a name="itconnectionget_networktype-method"></a><span data-ttu-id="39abf-103">Método ITConnection:: get \_ NetworkType</span><span class="sxs-lookup"><span data-stu-id="39abf-103">ITConnection::get\_NetworkType method</span></span>

<span data-ttu-id="39abf-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="39abf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="39abf-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="39abf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="39abf-106">O método **Get \_ NetworkType** Obtém o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="39abf-106">The **get\_NetworkType** method gets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="39abf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39abf-107">Syntax</span></span>


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="39abf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39abf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39abf-109">*ppNetworkType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="39abf-109">*ppNetworkType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39abf-110">Ponteiro para um **BSTR** que contém o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="39abf-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39abf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39abf-111">Return value</span></span>

<span data-ttu-id="39abf-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="39abf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="39abf-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="39abf-113">Return code</span></span>                                                                                   | <span data-ttu-id="39abf-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="39abf-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="39abf-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="39abf-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="39abf-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="39abf-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="39abf-118">O parâmetro *ppNetworkType* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="39abf-118">The *ppNetworkType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="39abf-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="39abf-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="39abf-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="39abf-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="39abf-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="39abf-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="39abf-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="39abf-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="39abf-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="39abf-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="39abf-125">Remarks</span></span>

<span data-ttu-id="39abf-126">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppNetworkType* .</span><span class="sxs-lookup"><span data-stu-id="39abf-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppNetworkType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="39abf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39abf-127">Requirements</span></span>



| <span data-ttu-id="39abf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="39abf-128">Requirement</span></span> | <span data-ttu-id="39abf-129">Valor</span><span class="sxs-lookup"><span data-stu-id="39abf-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39abf-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="39abf-130">TAPI version</span></span><br/> | <span data-ttu-id="39abf-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="39abf-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="39abf-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39abf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="39abf-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="39abf-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39abf-134">Library</span></span><br/>      | <dl> <span data-ttu-id="39abf-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="39abf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="39abf-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="39abf-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39abf-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39abf-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="39abf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39abf-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="39abf-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="39abf-140">**ITConnection::p UT \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="39abf-140">**ITConnection::put\_NetworkType**</span></span>](itconnection-put-networktype.md)
</dt> </dl>

 

