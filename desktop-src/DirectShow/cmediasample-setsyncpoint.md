---
description: 'O método SetSyncPoint especifica se o início deste exemplo é um ponto de sincronização. Esse método implementa o método IMediaSample:: SetSyncPoint.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Método CMediaSample. SetSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778619"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="e2c1a-104">Método CMediaSample. SetSyncPoint</span><span class="sxs-lookup"><span data-stu-id="e2c1a-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="e2c1a-105">O `SetSyncPoint` método especifica se o início deste exemplo é um ponto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="e2c1a-106">Esse método implementa o método [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="e2c1a-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c1a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2c1a-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="e2c1a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2c1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c1a-109">*bIsSyncPoint*</span><span class="sxs-lookup"><span data-stu-id="e2c1a-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="e2c1a-110">Valor booliano que especifica se este é um ponto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="e2c1a-111">Se for **true**, esse é um ponto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c1a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2c1a-112">Return value</span></span>

<span data-ttu-id="e2c1a-113">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c1a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2c1a-114">Remarks</span></span>

<span data-ttu-id="e2c1a-115">Esse método atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica a propriedade de ponto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c1a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2c1a-116">Requirements</span></span>



| <span data-ttu-id="e2c1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2c1a-117">Requirement</span></span> | <span data-ttu-id="e2c1a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e2c1a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c1a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2c1a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e2c1a-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2c1a-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2c1a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2c1a-121">Library</span></span><br/> | <dl> <span data-ttu-id="e2c1a-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e2c1a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c1a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2c1a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c1a-124">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




