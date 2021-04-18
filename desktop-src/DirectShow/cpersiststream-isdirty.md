---
description: Indica se o objeto foi alterado desde que foi salvo pela última vez em seu fluxo atual.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Método CPersistStream. IsDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754149"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="7bbc0-103">Método CPersistStream. IsDirty</span><span class="sxs-lookup"><span data-stu-id="7bbc0-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="7bbc0-104">Indica se o objeto foi alterado desde que foi salvo pela última vez em seu fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbc0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bbc0-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="7bbc0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bbc0-106">Parameters</span></span>

<span data-ttu-id="7bbc0-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bbc0-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7bbc0-108">Return value</span></span>

<span data-ttu-id="7bbc0-109">Retornará S \_ OK se o filtro precisar salvar e S \_ false se não precisar salvar.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bbc0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bbc0-110">Remarks</span></span>

<span data-ttu-id="7bbc0-111">Essa função de membro implementa o método **IPersistStream:: IsDirty** .</span><span class="sxs-lookup"><span data-stu-id="7bbc0-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbc0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bbc0-112">Requirements</span></span>



| <span data-ttu-id="7bbc0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bbc0-113">Requirement</span></span> | <span data-ttu-id="7bbc0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7bbc0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbc0-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7bbc0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7bbc0-116"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbc0-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7bbc0-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7bbc0-117">Library</span></span><br/> | <dl> <span data-ttu-id="7bbc0-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbc0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbc0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bbc0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbc0-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="7bbc0-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




