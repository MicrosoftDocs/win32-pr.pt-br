---
description: O \_ método Get originador Obtém o originador da conferência.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'Método ITSdp:: get_Originator (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766976"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="a0d40-103">Método ITSdp:: get \_ originador</span><span class="sxs-lookup"><span data-stu-id="a0d40-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="a0d40-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a0d40-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0d40-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a0d40-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a0d40-106">O método **Get \_ originador** Obtém o originador da conferência.</span><span class="sxs-lookup"><span data-stu-id="a0d40-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0d40-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="a0d40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0d40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0d40-109">*ppOriginator* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a0d40-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d40-110">Ponteiro para uma representação **BSTR** do originador da conferência.</span><span class="sxs-lookup"><span data-stu-id="a0d40-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0d40-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0d40-111">Return value</span></span>

<span data-ttu-id="a0d40-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a0d40-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a0d40-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a0d40-113">Return code</span></span>                                                                                   | <span data-ttu-id="a0d40-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0d40-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a0d40-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a0d40-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a0d40-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a0d40-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a0d40-118">O parâmetro *ppOriginator* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="a0d40-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a0d40-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a0d40-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a0d40-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a0d40-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a0d40-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a0d40-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a0d40-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a0d40-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="a0d40-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a0d40-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0d40-125">Remarks</span></span>

<span data-ttu-id="a0d40-126">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppOriginator* .</span><span class="sxs-lookup"><span data-stu-id="a0d40-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d40-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d40-127">Requirements</span></span>



| <span data-ttu-id="a0d40-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d40-128">Requirement</span></span> | <span data-ttu-id="a0d40-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a0d40-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d40-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a0d40-130">TAPI version</span></span><br/> | <span data-ttu-id="a0d40-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a0d40-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a0d40-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0d40-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a0d40-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0d40-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0d40-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a0d40-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a0d40-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0d40-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a0d40-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0d40-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d40-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0d40-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d40-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a0d40-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a0d40-140">**ITSdp::p o \_ remetente de UT**</span><span class="sxs-lookup"><span data-stu-id="a0d40-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

