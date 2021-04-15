---
description: O método Delete exclui o atributo no índice especificado.
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: 'ITAttributeList: método de:D xcluir (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729dd79b88198f671949aeb79caf06289abd9a75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753547"
---
# <a name="itattributelistdelete-method"></a><span data-ttu-id="8457f-103">ITAttributeList: método de:D xcluir</span><span class="sxs-lookup"><span data-stu-id="8457f-103">ITAttributeList::Delete method</span></span>

<span data-ttu-id="8457f-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8457f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8457f-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8457f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8457f-106">O método **delete** exclui o atributo no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8457f-106">The **Delete** method deletes the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8457f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8457f-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="8457f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8457f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8457f-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8457f-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8457f-110">Índice do atributo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8457f-110">Index of the attribute to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8457f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8457f-111">Return value</span></span>

<span data-ttu-id="8457f-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8457f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8457f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8457f-113">Return code</span></span>                                                                                   | <span data-ttu-id="8457f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8457f-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8457f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8457f-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8457f-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8457f-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8457f-118">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="8457f-118">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="8457f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8457f-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8457f-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8457f-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8457f-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8457f-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8457f-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8457f-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="8457f-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="8457f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8457f-125">Requirements</span></span>



| <span data-ttu-id="8457f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8457f-126">Requirement</span></span> | <span data-ttu-id="8457f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8457f-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8457f-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8457f-128">TAPI version</span></span><br/> | <span data-ttu-id="8457f-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8457f-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8457f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8457f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8457f-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8457f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8457f-132">Library</span></span><br/>      | <dl> <span data-ttu-id="8457f-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8457f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8457f-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="8457f-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8457f-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8457f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8457f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8457f-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="8457f-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




