---
description: 'O \_ método Get CurrentPosition recupera a posição atual, em relação à duração total do fluxo. Esse método implementa o método IMediaPosition:: get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Método de CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752085"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="82841-104">CPosPassThru. obter \_ método CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="82841-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="82841-105">O `get_CurrentPosition` método recupera a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="82841-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="82841-106">Esse método implementa o método [**IMediaPosition:: get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="82841-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82841-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82841-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="82841-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82841-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82841-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="82841-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="82841-110">Ponteiro para uma variável que recebe a posição atual, em segundos.</span><span class="sxs-lookup"><span data-stu-id="82841-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82841-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82841-111">Return value</span></span>

<span data-ttu-id="82841-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="82841-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="82841-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82841-113">Requirements</span></span>



| <span data-ttu-id="82841-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82841-114">Requirement</span></span> | <span data-ttu-id="82841-115">Valor</span><span class="sxs-lookup"><span data-stu-id="82841-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82841-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82841-116">Header</span></span><br/>  | <dl> <span data-ttu-id="82841-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82841-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82841-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82841-118">Library</span></span><br/> | <dl> <span data-ttu-id="82841-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="82841-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82841-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="82841-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82841-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="82841-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




