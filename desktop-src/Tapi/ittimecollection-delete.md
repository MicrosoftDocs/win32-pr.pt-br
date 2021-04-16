---
description: O método Delete exclui um componente ITTime.
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: 'ITTimeCollection: método de:D xcluir (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779305"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="c897c-103">ITTimeCollection: método de:D xcluir</span><span class="sxs-lookup"><span data-stu-id="c897c-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="c897c-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c897c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c897c-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c897c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c897c-106">O método **delete** exclui um componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="c897c-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="c897c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c897c-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="c897c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c897c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c897c-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c897c-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c897c-110">Índice do componente [**ITTime**](ittime.md) a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c897c-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="c897c-111">(A matriz de índice é baseada em um.)</span><span class="sxs-lookup"><span data-stu-id="c897c-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c897c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c897c-112">Return value</span></span>

<span data-ttu-id="c897c-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c897c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="c897c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c897c-114">Value</span></span>                                                                                         | <span data-ttu-id="c897c-115">Significado</span><span class="sxs-lookup"><span data-stu-id="c897c-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c897c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c897c-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c897c-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c897c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c897c-119">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="c897c-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="c897c-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c897c-121">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c897c-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c897c-122"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c897c-123">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c897c-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c897c-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c897c-125">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="c897c-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c897c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c897c-126">Requirements</span></span>



| <span data-ttu-id="c897c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c897c-127">Requirement</span></span> | <span data-ttu-id="c897c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c897c-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c897c-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c897c-129">TAPI version</span></span><br/> | <span data-ttu-id="c897c-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c897c-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c897c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c897c-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c897c-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c897c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c897c-133">Library</span></span><br/>      | <dl> <span data-ttu-id="c897c-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c897c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c897c-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="c897c-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c897c-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c897c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c897c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c897c-138">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="c897c-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="c897c-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="c897c-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




