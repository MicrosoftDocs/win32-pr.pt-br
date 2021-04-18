---
description: O \_ método Get atributolist Obtém a lista de atributos.
ms.assetid: 75518257-3339-441f-9965-b93e27f0e2bf
title: 'Método ITAttributeList:: get_AttributeList (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499352cd5087f478e58653fd304e27101db9b433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767759"
---
# <a name="itattributelistget_attributelist-method"></a><span data-ttu-id="c93e0-103">Método ITAttributeList:: get \_ atributolist</span><span class="sxs-lookup"><span data-stu-id="c93e0-103">ITAttributeList::get\_AttributeList method</span></span>

<span data-ttu-id="c93e0-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c93e0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c93e0-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c93e0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c93e0-106">O método **Get \_ atributolist** Obtém a lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="c93e0-106">The **get\_AttributeList** method gets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c93e0-107">Syntax</span></span>


```C++
HRESULT get_AttributeList(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c93e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c93e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93e0-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c93e0-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c93e0-110">Matriz de atributos.</span><span class="sxs-lookup"><span data-stu-id="c93e0-110">Array of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93e0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c93e0-111">Return value</span></span>

<span data-ttu-id="c93e0-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c93e0-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c93e0-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c93e0-113">Return code</span></span>                                                                                   | <span data-ttu-id="c93e0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c93e0-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c93e0-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c93e0-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c93e0-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c93e0-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c93e0-118">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="c93e0-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="c93e0-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c93e0-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c93e0-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c93e0-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c93e0-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c93e0-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c93e0-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c93e0-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="c93e0-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c93e0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c93e0-125">Requirements</span></span>



| <span data-ttu-id="c93e0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c93e0-126">Requirement</span></span> | <span data-ttu-id="c93e0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c93e0-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c93e0-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c93e0-128">TAPI version</span></span><br/> | <span data-ttu-id="c93e0-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c93e0-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c93e0-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c93e0-130">Header</span></span><br/>       | <dl> <span data-ttu-id="c93e0-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c93e0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c93e0-132">Library</span></span><br/>      | <dl> <span data-ttu-id="c93e0-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c93e0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c93e0-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="c93e0-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c93e0-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93e0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c93e0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93e0-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="c93e0-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="c93e0-138">**ITAttributeList::p UT \_ atributolist**</span><span class="sxs-lookup"><span data-stu-id="c93e0-138">**ITAttributeList::put\_AttributeList**</span></span>](itattributelist-put-attributelist.md)
</dt> </dl>

 

 




