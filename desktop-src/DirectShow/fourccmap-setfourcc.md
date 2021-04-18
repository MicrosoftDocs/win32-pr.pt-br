---
description: Define a parte FOURCC do objeto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Método FOURCCMap:: SetFOURCC (FOURCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796272"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="dd451-103">Método FOURCCMap:: SetFOURCC</span><span class="sxs-lookup"><span data-stu-id="dd451-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="dd451-104">Define a parte **FOURCC** do objeto [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="dd451-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd451-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd451-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="dd451-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd451-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="dd451-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="dd451-108">Ponteiro para a parte do identificador global exclusivo (**GUID**) retornado do objeto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="dd451-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd451-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd451-109">Return value</span></span>

<span data-ttu-id="dd451-110">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="dd451-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd451-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd451-111">Requirements</span></span>



| <span data-ttu-id="dd451-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd451-112">Requirement</span></span> | <span data-ttu-id="dd451-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dd451-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd451-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd451-114">Header</span></span><br/>  | <dl> <span data-ttu-id="dd451-115"><dt>FourCC. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd451-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dd451-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd451-116">Library</span></span><br/> | <dl> <span data-ttu-id="dd451-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dd451-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd451-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd451-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd451-119">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="dd451-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




