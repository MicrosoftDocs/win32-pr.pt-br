---
description: Construtor de CBaseControlVideo. CBaseControlVideo-método de construtor.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Construtor CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096344"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="47108-103">Construtor CBaseControlVideo. CBaseControlVideo</span><span class="sxs-lookup"><span data-stu-id="47108-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="47108-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="47108-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47108-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47108-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="47108-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47108-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47108-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="47108-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="47108-108">Ponteiro para o objeto de filtro de mídia proprietário.</span><span class="sxs-lookup"><span data-stu-id="47108-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="47108-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="47108-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="47108-110">Ponteiro para a seção crítica a ser usada para bloqueio.</span><span class="sxs-lookup"><span data-stu-id="47108-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="47108-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="47108-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="47108-112">Ponteiro para a descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="47108-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="47108-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="47108-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="47108-114">Ponteiro para a interface **IUnknown** de controle, se o objeto fizer parte de uma agregação; caso contrário, deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="47108-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47108-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="47108-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="47108-116">Ponteiro para uma variável que recebe um valor HRESULT que indica o êxito ou a falha do método de construtor.</span><span class="sxs-lookup"><span data-stu-id="47108-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47108-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="47108-117">Remarks</span></span>

<span data-ttu-id="47108-118">O objeto implementa a interface de controle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="47108-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="47108-119">Todos os métodos de interface de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) que essa classe implementa exigem que o filtro esteja conectado corretamente.</span><span class="sxs-lookup"><span data-stu-id="47108-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="47108-120">Por esse motivo, a classe recebe um PIN com o qual ele deve sincronizar.</span><span class="sxs-lookup"><span data-stu-id="47108-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="47108-121">Sempre que um método de interface é chamado, o objeto determina que o PIN ainda está conectado.</span><span class="sxs-lookup"><span data-stu-id="47108-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="47108-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47108-122">Requirements</span></span>



| <span data-ttu-id="47108-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="47108-123">Requirement</span></span> | <span data-ttu-id="47108-124">Valor</span><span class="sxs-lookup"><span data-stu-id="47108-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47108-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47108-125">Header</span></span><br/>  | <dl> <span data-ttu-id="47108-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47108-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47108-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47108-127">Library</span></span><br/> | <dl> <span data-ttu-id="47108-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="47108-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47108-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="47108-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47108-130">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="47108-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




