---
description: O método Exit sinaliza o thread de streaming para sair.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Método CSourceStream. Exit (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747588"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="6cdc8-103">Método CSourceStream. Exit</span><span class="sxs-lookup"><span data-stu-id="6cdc8-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="6cdc8-104">O `Exit` método sinaliza o thread de streaming para sair.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cdc8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cdc8-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="6cdc8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cdc8-106">Parameters</span></span>

<span data-ttu-id="6cdc8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cdc8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cdc8-108">Return value</span></span>

<span data-ttu-id="6cdc8-109">Retorna S \_ OK ou E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cdc8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cdc8-110">Remarks</span></span>

<span data-ttu-id="6cdc8-111">O método [**CSourceStream:: Inactive**](csourcestream-inactive.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="6cdc8-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cdc8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cdc8-112">Requirements</span></span>



| <span data-ttu-id="6cdc8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cdc8-113">Requirement</span></span> | <span data-ttu-id="6cdc8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6cdc8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc8-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cdc8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6cdc8-116"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cdc8-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6cdc8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cdc8-117">Library</span></span><br/> | <dl> <span data-ttu-id="6cdc8-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6cdc8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cdc8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cdc8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cdc8-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="6cdc8-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




