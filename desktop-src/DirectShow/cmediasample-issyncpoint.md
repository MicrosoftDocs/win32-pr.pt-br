---
description: 'O método IsSyncPoint determina se o início do exemplo é um ponto de sincronização. Esse método implementa o método IMediaSample:: IsSyncPoint.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Método CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756626"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="1e15e-104">Método CMediaSample. IsSyncPoint</span><span class="sxs-lookup"><span data-stu-id="1e15e-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="1e15e-105">O `IsSyncPoint` método determina se o início do exemplo é um ponto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1e15e-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="1e15e-106">Esse método implementa o método [**IMediaSample:: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="1e15e-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e15e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e15e-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="1e15e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e15e-108">Parameters</span></span>

<span data-ttu-id="1e15e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e15e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e15e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e15e-110">Return value</span></span>

<span data-ttu-id="1e15e-111">Retorna S \_ OK se o exemplo for um ponto de sincronização, \_ caso contrário, s false.</span><span class="sxs-lookup"><span data-stu-id="1e15e-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e15e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e15e-112">Remarks</span></span>

<span data-ttu-id="1e15e-113">A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e15e-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e15e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e15e-114">Requirements</span></span>



| <span data-ttu-id="1e15e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e15e-115">Requirement</span></span> | <span data-ttu-id="1e15e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1e15e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e15e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e15e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1e15e-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e15e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1e15e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e15e-119">Library</span></span><br/> | <dl> <span data-ttu-id="1e15e-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1e15e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e15e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e15e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e15e-122">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="1e15e-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




