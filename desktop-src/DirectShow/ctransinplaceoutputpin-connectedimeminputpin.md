---
description: 'O método ConnectedIMemInputPin recupera um ponteiro para o pino de entrada downstream. Esse método retorna a variável de membro CBaseOutputPin:: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Método CTransInPlaceOutputPin. ConnectedIMemInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752279"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="7aaf2-104">Método CTransInPlaceOutputPin. ConnectedIMemInputPin</span><span class="sxs-lookup"><span data-stu-id="7aaf2-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="7aaf2-105">O `ConnectedIMemInputPin` método recupera um ponteiro para o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="7aaf2-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="7aaf2-106">Esse método retorna a variável de membro [**CBaseOutputPin:: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7aaf2-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aaf2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7aaf2-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="7aaf2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7aaf2-108">Parameters</span></span>

<span data-ttu-id="7aaf2-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7aaf2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7aaf2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7aaf2-110">Return value</span></span>

<span data-ttu-id="7aaf2-111">Retorna um ponteiro para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="7aaf2-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aaf2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aaf2-112">Requirements</span></span>



| <span data-ttu-id="7aaf2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aaf2-113">Requirement</span></span> | <span data-ttu-id="7aaf2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7aaf2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aaf2-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7aaf2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7aaf2-116"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf2-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7aaf2-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7aaf2-117">Library</span></span><br/> | <dl> <span data-ttu-id="7aaf2-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aaf2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aaf2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aaf2-120">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7aaf2-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




