---
description: 'O método setnotificate define ou remove um retorno de chamada no alocador. O alocador chama o método de retorno de chamada sempre que o método IMemAllocator:: ReleaseBuffer do alocador é chamado.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Método CBaseAllocator. setnotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756000"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="d02f9-104">Método CBaseAllocator. setnotificar</span><span class="sxs-lookup"><span data-stu-id="d02f9-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="d02f9-105">\[[**Setnotificar**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) pode ser alterado ou indisponível nas versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="d02f9-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d02f9-106">O `SetNotify` método define ou remove um retorno de chamada no alocador.</span><span class="sxs-lookup"><span data-stu-id="d02f9-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="d02f9-107">O alocador chama o método de retorno de chamada sempre que o método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) do alocador é chamado.</span><span class="sxs-lookup"><span data-stu-id="d02f9-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02f9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d02f9-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="d02f9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d02f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02f9-110">*pNotify*</span><span class="sxs-lookup"><span data-stu-id="d02f9-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="d02f9-111">Ponteiro para a interface [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) que será usada para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d02f9-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="d02f9-112">O chamador deve implementar a interface.</span><span class="sxs-lookup"><span data-stu-id="d02f9-112">The caller must implement the interface.</span></span> <span data-ttu-id="d02f9-113">Use o valor **NULL** para remover o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d02f9-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02f9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d02f9-114">Return value</span></span>

<span data-ttu-id="d02f9-115">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d02f9-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d02f9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d02f9-116">Remarks</span></span>

<span data-ttu-id="d02f9-117">Esse método implementa o método [**IMemAllocatorCallbackTemp:: Setnotificar**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) .</span><span class="sxs-lookup"><span data-stu-id="d02f9-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="d02f9-118">O alocador não expõe a interface [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , a menos que o sinalizador *fEnableReleaseCallback* seja definido como **true** no construtor [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="d02f9-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="d02f9-119">Esse método define a variável de membro [**CBaseAllocator:: m \_ pNotify**](cbaseallocator-m-pnotify.md) igual a *pNotify* e incrementa a contagem de referência na interface.</span><span class="sxs-lookup"><span data-stu-id="d02f9-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="d02f9-120">Se *m \_ pNotify* for não **nulo**, o método **ReleaseBuffer** do alocador chamará [**IMemAllocatorNotifyCallbackTemp:: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span><span class="sxs-lookup"><span data-stu-id="d02f9-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="d02f9-121">Consulte a seção comentários nesse método para obter informações sobre como implementar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d02f9-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="d02f9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d02f9-122">Requirements</span></span>



| <span data-ttu-id="d02f9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d02f9-123">Requirement</span></span> | <span data-ttu-id="d02f9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d02f9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d02f9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d02f9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d02f9-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d02f9-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d02f9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d02f9-127">Library</span></span><br/> | <dl> <span data-ttu-id="d02f9-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d02f9-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02f9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d02f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02f9-130">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="d02f9-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




