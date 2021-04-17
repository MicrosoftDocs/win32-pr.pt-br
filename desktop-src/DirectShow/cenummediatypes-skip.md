---
description: 'O método Skip ignora um número especificado de tipos de mídia. Esse método implementa o método IEnumMediaTypes:: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Método CEnumMediaTypes. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748205"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="fd353-104">Método CEnumMediaTypes. Skip</span><span class="sxs-lookup"><span data-stu-id="fd353-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="fd353-105">O `Skip` método ignora um número especificado de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="fd353-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="fd353-106">Esse método implementa o método [**IEnumMediaTypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .</span><span class="sxs-lookup"><span data-stu-id="fd353-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd353-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd353-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="fd353-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd353-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="fd353-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="fd353-110">Número de tipos de mídia a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="fd353-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd353-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd353-111">Return value</span></span>

<span data-ttu-id="fd353-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd353-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="fd353-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fd353-113">Return code</span></span>                                                                                                | <span data-ttu-id="fd353-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd353-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd353-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="fd353-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="fd353-116">Ignorado após o fim da sequência.</span><span class="sxs-lookup"><span data-stu-id="fd353-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fd353-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd353-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="fd353-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="fd353-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="fd353-119"><dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt></span><span class="sxs-lookup"><span data-stu-id="fd353-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="fd353-120">O estado do PIN foi alterado e agora está inconsistente com o enumerador.</span><span class="sxs-lookup"><span data-stu-id="fd353-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fd353-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd353-121">Requirements</span></span>



| <span data-ttu-id="fd353-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd353-122">Requirement</span></span> | <span data-ttu-id="fd353-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fd353-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd353-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd353-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fd353-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd353-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fd353-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd353-126">Library</span></span><br/> | <dl> <span data-ttu-id="fd353-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fd353-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd353-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd353-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd353-129">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="fd353-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




