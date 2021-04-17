---
description: O \_ método Get AddressType Obtém o tipo de endereço.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'Método ITConnection:: get_AddressType (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780603"
---
# <a name="itconnectionget_addresstype-method"></a><span data-ttu-id="3ef5c-103">Método ITConnection:: get \_ AddressType</span><span class="sxs-lookup"><span data-stu-id="3ef5c-103">ITConnection::get\_AddressType method</span></span>

<span data-ttu-id="3ef5c-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3ef5c-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3ef5c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3ef5c-106">O método **Get \_ AddressType** Obtém o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-106">The **get\_AddressType** method gets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef5c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ef5c-107">Syntax</span></span>


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="3ef5c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ef5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ef5c-109">*ppAddressType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ef5c-109">*ppAddressType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef5c-110">Ponteiro para um **BSTR** que contém o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ef5c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ef5c-111">Return value</span></span>

<span data-ttu-id="3ef5c-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3ef5c-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3ef5c-113">Return code</span></span>                                                                                   | <span data-ttu-id="3ef5c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ef5c-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ef5c-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3ef5c-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3ef5c-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3ef5c-118">O parâmetro *ppAddressType* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-118">The *ppAddressType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="3ef5c-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3ef5c-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="3ef5c-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3ef5c-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3ef5c-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3ef5c-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="3ef5c-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="3ef5c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ef5c-125">Remarks</span></span>

<span data-ttu-id="3ef5c-126">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppAddressType* .</span><span class="sxs-lookup"><span data-stu-id="3ef5c-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppAddressType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef5c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ef5c-127">Requirements</span></span>



| <span data-ttu-id="3ef5c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef5c-128">Requirement</span></span> | <span data-ttu-id="3ef5c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3ef5c-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef5c-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3ef5c-130">TAPI version</span></span><br/> | <span data-ttu-id="3ef5c-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3ef5c-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3ef5c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ef5c-132">Header</span></span><br/>       | <dl> <span data-ttu-id="3ef5c-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ef5c-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ef5c-134">Library</span></span><br/>      | <dl> <span data-ttu-id="3ef5c-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3ef5c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3ef5c-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="3ef5c-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ef5c-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef5c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ef5c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef5c-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="3ef5c-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="3ef5c-140">**ITConnection::p UT \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="3ef5c-140">**ITConnection::put\_AddressType**</span></span>](itconnection-put-addresstype.md)
</dt> </dl>

 

