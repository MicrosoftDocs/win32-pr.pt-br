---
description: Determina se um retângulo de origem é válido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Método CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749857"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="047f4-103">Método CBaseControlVideo. CheckSourceRect</span><span class="sxs-lookup"><span data-stu-id="047f4-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="047f4-104">Determina se um retângulo de origem é válido.</span><span class="sxs-lookup"><span data-stu-id="047f4-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="047f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="047f4-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="047f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="047f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="047f4-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="047f4-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="047f4-108">Ponteiro para o retângulo de origem a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="047f4-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="047f4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="047f4-109">Return value</span></span>

<span data-ttu-id="047f4-110">Retorna E \_ INVALIDARG se não for válido; caso contrário, retornará NOERROR (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="047f4-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="047f4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="047f4-111">Remarks</span></span>

<span data-ttu-id="047f4-112">Essa função de membro verifica se o retângulo de origem solicitado não excede o vídeo de origem disponível.</span><span class="sxs-lookup"><span data-stu-id="047f4-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="047f4-113">As coordenadas esquerda e superior não podem ser negativas e a largura e a altura não podem exceder a direita e a parte inferior do vídeo.</span><span class="sxs-lookup"><span data-stu-id="047f4-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="047f4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="047f4-114">Requirements</span></span>



| <span data-ttu-id="047f4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="047f4-115">Requirement</span></span> | <span data-ttu-id="047f4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="047f4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047f4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="047f4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="047f4-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="047f4-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="047f4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="047f4-119">Library</span></span><br/> | <dl> <span data-ttu-id="047f4-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="047f4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047f4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="047f4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047f4-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="047f4-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




