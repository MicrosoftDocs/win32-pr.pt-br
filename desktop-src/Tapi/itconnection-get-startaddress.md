---
description: O \_ método Get StartAddress Obtém o primeiro endereço a ser usado para a sessão.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Método ITConnection:: get_StartAddress (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810466"
---
# <a name="itconnectionget_startaddress-method"></a><span data-ttu-id="82641-103">Método StartAddress ITConnection:: get \_</span><span class="sxs-lookup"><span data-stu-id="82641-103">ITConnection::get\_StartAddress method</span></span>

<span data-ttu-id="82641-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="82641-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="82641-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="82641-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="82641-106">O método **Get \_ StartAddress** Obtém o primeiro endereço a ser usado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="82641-106">The **get\_StartAddress** method gets the first address to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="82641-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82641-107">Syntax</span></span>


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a><span data-ttu-id="82641-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82641-109">*ppStartAddress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="82641-109">*ppStartAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82641-110">Ponteiro para um **BSTR** que contém o endereço inicial da sessão.</span><span class="sxs-lookup"><span data-stu-id="82641-110">Pointer to a **BSTR** containing the starting address for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82641-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82641-111">Return value</span></span>

<span data-ttu-id="82641-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="82641-112">This method can return one of these values.</span></span>



| <span data-ttu-id="82641-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="82641-113">Return code</span></span>                                                                                   | <span data-ttu-id="82641-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="82641-114">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="82641-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82641-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82641-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="82641-116">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="82641-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="82641-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="82641-118">O parâmetro *ppStartAddress* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="82641-118">The *ppStartAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="82641-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82641-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82641-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="82641-120">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="82641-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="82641-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="82641-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="82641-122">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="82641-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="82641-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="82641-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="82641-124">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="82641-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="82641-125">Remarks</span></span>

<span data-ttu-id="82641-126">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppStartAddress* .</span><span class="sxs-lookup"><span data-stu-id="82641-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppStartAddress* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="82641-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82641-127">Requirements</span></span>



| <span data-ttu-id="82641-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="82641-128">Requirement</span></span> | <span data-ttu-id="82641-129">Valor</span><span class="sxs-lookup"><span data-stu-id="82641-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82641-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="82641-130">TAPI version</span></span><br/> | <span data-ttu-id="82641-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="82641-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="82641-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82641-132">Header</span></span><br/>       | <dl> <span data-ttu-id="82641-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="82641-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="82641-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82641-134">Library</span></span><br/>      | <dl> <span data-ttu-id="82641-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82641-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="82641-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82641-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="82641-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82641-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82641-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="82641-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82641-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="82641-139">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

