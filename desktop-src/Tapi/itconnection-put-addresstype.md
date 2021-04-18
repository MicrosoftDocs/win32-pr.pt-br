---
description: O \_ método Put AddressType define o tipo de endereço.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: 'ITConnection: método de ut_AddressType de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757214"
---
# <a name="itconnectionput_addresstype-method"></a><span data-ttu-id="cb694-103">Método ITConnection::p UT \_ AddressType</span><span class="sxs-lookup"><span data-stu-id="cb694-103">ITConnection::put\_AddressType method</span></span>

<span data-ttu-id="cb694-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cb694-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cb694-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cb694-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cb694-106">O método **Put \_ AddressType** define o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="cb694-106">The **put\_AddressType** method sets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb694-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb694-107">Syntax</span></span>


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="cb694-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb694-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb694-109">*pAddressType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb694-109">*pAddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb694-110">Ponteiro para um **BSTR** que contém o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="cb694-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb694-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb694-111">Return value</span></span>

<span data-ttu-id="cb694-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cb694-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cb694-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cb694-113">Return code</span></span>                                                                                   | <span data-ttu-id="cb694-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb694-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cb694-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cb694-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cb694-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cb694-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cb694-118">O parâmetro *pAddressType* não é válido.</span><span class="sxs-lookup"><span data-stu-id="cb694-118">The *pAddressType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="cb694-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cb694-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="cb694-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cb694-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cb694-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="cb694-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cb694-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cb694-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="cb694-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cb694-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb694-125">Remarks</span></span>

<span data-ttu-id="cb694-126">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PAddressType* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="cb694-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAddressType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb694-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb694-127">Requirements</span></span>



| <span data-ttu-id="cb694-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb694-128">Requirement</span></span> | <span data-ttu-id="cb694-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cb694-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb694-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cb694-130">TAPI version</span></span><br/> | <span data-ttu-id="cb694-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cb694-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cb694-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb694-132">Header</span></span><br/>       | <dl> <span data-ttu-id="cb694-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb694-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb694-134">Library</span></span><br/>      | <dl> <span data-ttu-id="cb694-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cb694-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cb694-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="cb694-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb694-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb694-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb694-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb694-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="cb694-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="cb694-140">**ITConnection:: obter \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="cb694-140">**ITConnection::get\_AddressType**</span></span>](itconnection-get-addresstype.md)
</dt> </dl>

 

