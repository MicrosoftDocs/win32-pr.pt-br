---
description: 'Método ITMediaCollection:: get__NewEnum-o \_ \_ método Get NewEnum retorna um enumerador para a coleção.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'Método ITMediaCollection:: get__NewEnum (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6683ce0a00f0128cb959dd5a2c39e8b06382f65d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098354"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="ca3e8-103">\_Método NewEnum ITMediaCollection:: get \_</span><span class="sxs-lookup"><span data-stu-id="ca3e8-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="ca3e8-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ca3e8-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ca3e8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ca3e8-106">O método **Get \_ \_ NewEnum** retorna um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca3e8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca3e8-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ca3e8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca3e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca3e8-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca3e8-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca3e8-110">Ponteiro para uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) em um objeto enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="ca3e8-111">Chame o método [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface **IUnknown** retornada para obter um ponteiro para uma interface de enumeração [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) na coleção.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="ca3e8-112">O **IEnumVARIANT** fornece vários métodos que você pode usar para iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="ca3e8-113">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca3e8-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ca3e8-114">Return value</span></span>

<span data-ttu-id="ca3e8-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ca3e8-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ca3e8-116">Return code</span></span>                                                                                   | <span data-ttu-id="ca3e8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca3e8-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ca3e8-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ca3e8-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ca3e8-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ca3e8-121">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="ca3e8-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ca3e8-123">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ca3e8-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ca3e8-125">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ca3e8-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ca3e8-127">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="ca3e8-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="ca3e8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca3e8-128">Remarks</span></span>

<span data-ttu-id="ca3e8-129">Esse método é intercambiável com [**Get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) , exceto pelo fato de que ele retorna **IUnknown** em vez de [**IEnumMedia**](ienummedia.md).</span><span class="sxs-lookup"><span data-stu-id="ca3e8-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca3e8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca3e8-130">Requirements</span></span>



| <span data-ttu-id="ca3e8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca3e8-131">Requirement</span></span> | <span data-ttu-id="ca3e8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ca3e8-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca3e8-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ca3e8-133">TAPI version</span></span><br/> | <span data-ttu-id="ca3e8-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ca3e8-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ca3e8-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca3e8-135">Header</span></span><br/>       | <dl> <span data-ttu-id="ca3e8-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca3e8-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca3e8-137">Library</span></span><br/>      | <dl> <span data-ttu-id="ca3e8-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ca3e8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ca3e8-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="ca3e8-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca3e8-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca3e8-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ca3e8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca3e8-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="ca3e8-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

