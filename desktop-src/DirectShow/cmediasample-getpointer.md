---
description: 'O método getapontarr recupera um ponteiro de leitura/gravação para o buffer. Esse método implementa o método IMediaSample:: getapontarr.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Método CMediaSample. GetPointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757316"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="688cb-104">Método CMediaSample. GetPointer</span><span class="sxs-lookup"><span data-stu-id="688cb-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="688cb-105">O `GetPointer` método recupera um ponteiro de leitura/gravação para o buffer.</span><span class="sxs-lookup"><span data-stu-id="688cb-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="688cb-106">Esse método implementa o método [**IMediaSample:: Getapontarr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) .</span><span class="sxs-lookup"><span data-stu-id="688cb-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="688cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="688cb-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="688cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="688cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="688cb-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="688cb-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="688cb-110">Endereço de uma variável que recebe um ponteiro para o buffer.</span><span class="sxs-lookup"><span data-stu-id="688cb-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="688cb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="688cb-111">Return value</span></span>

<span data-ttu-id="688cb-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="688cb-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="688cb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="688cb-113">Requirements</span></span>



| <span data-ttu-id="688cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="688cb-114">Requirement</span></span> | <span data-ttu-id="688cb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="688cb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688cb-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="688cb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="688cb-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="688cb-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="688cb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="688cb-118">Library</span></span><br/> | <dl> <span data-ttu-id="688cb-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="688cb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="688cb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="688cb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688cb-121">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="688cb-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




