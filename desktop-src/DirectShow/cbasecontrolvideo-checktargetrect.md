---
description: O método CheckTargetRect determina se um retângulo de destino é válido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Método CBaseControlVideo. CheckTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759917"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="0c4da-103">Método CBaseControlVideo. CheckTargetRect</span><span class="sxs-lookup"><span data-stu-id="0c4da-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="0c4da-104">O `CheckTargetRect` método determina se um retângulo de destino é válido.</span><span class="sxs-lookup"><span data-stu-id="0c4da-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4da-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c4da-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="0c4da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c4da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4da-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="0c4da-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4da-108">Ponteiro para o retângulo de destino a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="0c4da-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4da-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c4da-109">Return value</span></span>

<span data-ttu-id="0c4da-110">Retorna E \_ INVALIDARG se não for válido; caso contrário, retornará NOERROR (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="0c4da-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4da-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c4da-111">Remarks</span></span>

<span data-ttu-id="0c4da-112">Essa função de membro determina se o retângulo de destino solicitado é válido.</span><span class="sxs-lookup"><span data-stu-id="0c4da-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="0c4da-113">Como o retângulo de destino especifica uma posição no cliente lógico da janela, as coordenadas podem ser negativas, embora a largura e a altura gerais não possam ser zero ou um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="0c4da-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4da-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c4da-114">Requirements</span></span>



| <span data-ttu-id="0c4da-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c4da-115">Requirement</span></span> | <span data-ttu-id="0c4da-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0c4da-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4da-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c4da-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0c4da-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c4da-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c4da-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c4da-119">Library</span></span><br/> | <dl> <span data-ttu-id="0c4da-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0c4da-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c4da-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c4da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4da-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="0c4da-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




