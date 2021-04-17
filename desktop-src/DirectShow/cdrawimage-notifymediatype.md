---
description: O método NotifyMediaType notifica o objeto CDrawImage do tipo de mídia atual.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Método CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770101"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="64955-103">Método CDrawImage. NotifyMediaType</span><span class="sxs-lookup"><span data-stu-id="64955-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="64955-104">O `NotifyMediaType` método notifica o objeto **CDrawImage** do tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="64955-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="64955-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64955-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="64955-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64955-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64955-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="64955-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="64955-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) ou **NULL** para limpar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="64955-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64955-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64955-109">Return value</span></span>

<span data-ttu-id="64955-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="64955-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64955-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="64955-111">Remarks</span></span>

<span data-ttu-id="64955-112">O filtro proprietário deve chamar esse método sempre que o tipo de mídia for alterado.</span><span class="sxs-lookup"><span data-stu-id="64955-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="64955-113">Normalmente, isso ocorre quando o PIN se conecta pela primeira vez e após uma alteração de formato dinâmico.</span><span class="sxs-lookup"><span data-stu-id="64955-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="64955-114">O objeto **CDrawImage** armazena o ponteiro *pMediaType* na variável de membro **m \_ pMediaType** .</span><span class="sxs-lookup"><span data-stu-id="64955-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="64955-115">Portanto, se o chamador precisar liberar o objeto **CMediaType** , ele deverá atualizar o objeto **CDrawImage** chamando esse método novamente, seja com um novo ponteiro ou com um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="64955-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="64955-116">Caso contrário, poderá ocorrer um erro quando o objeto **CDrawImage** tentar referenciar o ponteiro antigo.</span><span class="sxs-lookup"><span data-stu-id="64955-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="64955-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64955-117">Requirements</span></span>



| <span data-ttu-id="64955-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="64955-118">Requirement</span></span> | <span data-ttu-id="64955-119">Valor</span><span class="sxs-lookup"><span data-stu-id="64955-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64955-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64955-120">Header</span></span><br/>  | <dl> <span data-ttu-id="64955-121"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64955-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="64955-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64955-122">Library</span></span><br/> | <dl> <span data-ttu-id="64955-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="64955-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64955-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="64955-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64955-125">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="64955-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




