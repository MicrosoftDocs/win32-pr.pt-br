---
description: 'O método Skip ignora um número especificado de Pins na sequência de enumeração. Esse método implementa o método IEnumPins:: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Método CEnumPins. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770290"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="e983a-104">Método CEnumPins. Skip</span><span class="sxs-lookup"><span data-stu-id="e983a-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="e983a-105">O `Skip` método ignora um número especificado de Pins na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="e983a-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="e983a-106">Esse método implementa o método [**IEnumPins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .</span><span class="sxs-lookup"><span data-stu-id="e983a-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e983a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e983a-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="e983a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e983a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e983a-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="e983a-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="e983a-110">Número de Pins a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="e983a-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e983a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e983a-111">Return value</span></span>

<span data-ttu-id="e983a-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e983a-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e983a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e983a-113">Return code</span></span>                                                                                                | <span data-ttu-id="e983a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e983a-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e983a-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="e983a-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="e983a-116">Ignorado após o fim da sequência.</span><span class="sxs-lookup"><span data-stu-id="e983a-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="e983a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e983a-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e983a-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="e983a-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="e983a-119"><dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt></span><span class="sxs-lookup"><span data-stu-id="e983a-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="e983a-120">O estado do filtro foi alterado e agora está inconsistente com o enumerador.</span><span class="sxs-lookup"><span data-stu-id="e983a-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e983a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e983a-121">Requirements</span></span>



| <span data-ttu-id="e983a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e983a-122">Requirement</span></span> | <span data-ttu-id="e983a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e983a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e983a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e983a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e983a-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e983a-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e983a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e983a-126">Library</span></span><br/> | <dl> <span data-ttu-id="e983a-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e983a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e983a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e983a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e983a-129">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="e983a-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




