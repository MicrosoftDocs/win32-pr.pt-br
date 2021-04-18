---
description: O \_ \_ método Get NewEnum retorna um enumerador para a coleção.
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'Método ITMediaCollection:: get__NewEnum (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfa5655d70026fe2c481aedad0e76923f4caa646
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760162"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="987d4-103">\_Método NewEnum ITMediaCollection:: get \_</span><span class="sxs-lookup"><span data-stu-id="987d4-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="987d4-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="987d4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="987d4-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="987d4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="987d4-106">O método **Get \_ \_ NewEnum** retorna um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="987d4-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="987d4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="987d4-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="987d4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="987d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="987d4-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="987d4-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="987d4-110">Ponteiro para uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) em um objeto enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="987d4-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="987d4-111">Chame o método [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface **IUnknown** retornada para obter um ponteiro para uma interface de enumeração [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) na coleção.</span><span class="sxs-lookup"><span data-stu-id="987d4-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="987d4-112">O **IEnumVARIANT** fornece vários métodos que você pode usar para iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="987d4-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="987d4-113">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="987d4-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="987d4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="987d4-114">Return value</span></span>

<span data-ttu-id="987d4-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="987d4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="987d4-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="987d4-116">Return code</span></span>                                                                                   | <span data-ttu-id="987d4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="987d4-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="987d4-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="987d4-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="987d4-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="987d4-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="987d4-121">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="987d4-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="987d4-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="987d4-123">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="987d4-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="987d4-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="987d4-125">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="987d4-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="987d4-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="987d4-127">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="987d4-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="987d4-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="987d4-128">Remarks</span></span>

<span data-ttu-id="987d4-129">Esse método é intercambiável com [**Get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) , exceto pelo fato de que ele retorna **IUnknown** em vez de [**IEnumMedia**](ienummedia.md).</span><span class="sxs-lookup"><span data-stu-id="987d4-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="987d4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="987d4-130">Requirements</span></span>



| <span data-ttu-id="987d4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="987d4-131">Requirement</span></span> | <span data-ttu-id="987d4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="987d4-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="987d4-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="987d4-133">TAPI version</span></span><br/> | <span data-ttu-id="987d4-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="987d4-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="987d4-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="987d4-135">Header</span></span><br/>       | <dl> <span data-ttu-id="987d4-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="987d4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="987d4-137">Library</span></span><br/>      | <dl> <span data-ttu-id="987d4-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="987d4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="987d4-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="987d4-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="987d4-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987d4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="987d4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987d4-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="987d4-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

