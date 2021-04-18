---
description: 'O método GetProperties recupera as propriedades do exemplo. Esse método implementa o método IMediaSample2:: GetProperties.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Método CMediaSample. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778622"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="edc7a-104">Método CMediaSample. GetProperties</span><span class="sxs-lookup"><span data-stu-id="edc7a-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="edc7a-105">O `GetProperties` método recupera as propriedades do exemplo.</span><span class="sxs-lookup"><span data-stu-id="edc7a-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="edc7a-106">Esse método implementa o método [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="edc7a-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc7a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edc7a-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="edc7a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edc7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc7a-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="edc7a-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="edc7a-110">Comprimento dos dados de propriedade a serem recuperados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="edc7a-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="edc7a-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="edc7a-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="edc7a-112">Ponteiro para um buffer de tamanho *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="edc7a-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc7a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edc7a-113">Return value</span></span>

<span data-ttu-id="edc7a-114">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="edc7a-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="edc7a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="edc7a-115">Return code</span></span>                                                                               | <span data-ttu-id="edc7a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="edc7a-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="edc7a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="edc7a-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="edc7a-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="edc7a-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="edc7a-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="edc7a-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="edc7a-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="edc7a-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="edc7a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edc7a-121">Requirements</span></span>



| <span data-ttu-id="edc7a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc7a-122">Requirement</span></span> | <span data-ttu-id="edc7a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="edc7a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc7a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="edc7a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="edc7a-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edc7a-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="edc7a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edc7a-126">Library</span></span><br/> | <dl> <span data-ttu-id="edc7a-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="edc7a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc7a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="edc7a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc7a-129">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="edc7a-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




