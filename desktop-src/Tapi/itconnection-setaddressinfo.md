---
description: O método SetAddressInfo define as informações de endereço.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'Método ITConnection:: SetAddressInfo (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767757"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="70181-103">Método ITConnection:: SetAddressInfo</span><span class="sxs-lookup"><span data-stu-id="70181-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="70181-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="70181-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70181-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="70181-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="70181-106">O método **SetAddressInfo** define as informações de endereço.</span><span class="sxs-lookup"><span data-stu-id="70181-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="70181-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70181-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="70181-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70181-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70181-109">*pStartAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70181-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70181-110">Ponteiro para um **BSTR** que contém o endereço inicial.</span><span class="sxs-lookup"><span data-stu-id="70181-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="70181-111">*NumAddresses* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70181-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70181-112">Número de endereços a serem usados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="70181-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="70181-113">*TTL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70181-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70181-114">escopo [*TTL (vida útil)*](t-tapgloss.md) para transmissões nos endereços.</span><span class="sxs-lookup"><span data-stu-id="70181-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70181-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70181-115">Return value</span></span>

<span data-ttu-id="70181-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="70181-116">This method can return one of these values.</span></span>



| <span data-ttu-id="70181-117">Valor</span><span class="sxs-lookup"><span data-stu-id="70181-117">Value</span></span>                                                                                         | <span data-ttu-id="70181-118">Significado</span><span class="sxs-lookup"><span data-stu-id="70181-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70181-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="70181-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="70181-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="70181-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="70181-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="70181-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="70181-122">O parâmetro *pStartAddress*, *NumAddresses* ou *TTL* não é válido.</span><span class="sxs-lookup"><span data-stu-id="70181-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="70181-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="70181-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="70181-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="70181-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="70181-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="70181-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="70181-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="70181-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="70181-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="70181-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="70181-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="70181-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="70181-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="70181-129">Remarks</span></span>

<span data-ttu-id="70181-130">O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PStartAddress* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="70181-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="70181-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70181-131">Requirements</span></span>



| <span data-ttu-id="70181-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="70181-132">Requirement</span></span> | <span data-ttu-id="70181-133">Valor</span><span class="sxs-lookup"><span data-stu-id="70181-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70181-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="70181-134">TAPI version</span></span><br/> | <span data-ttu-id="70181-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="70181-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="70181-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70181-136">Header</span></span><br/>       | <dl> <span data-ttu-id="70181-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="70181-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="70181-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70181-138">Library</span></span><br/>      | <dl> <span data-ttu-id="70181-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70181-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="70181-140">DLL</span><span class="sxs-lookup"><span data-stu-id="70181-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="70181-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70181-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70181-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="70181-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70181-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="70181-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

