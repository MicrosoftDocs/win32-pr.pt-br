---
description: A função isequalobject verifica se duas interfaces estão no mesmo objeto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Função isequalobject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784021"
---
# <a name="isequalobject-function"></a><span data-ttu-id="b2c41-103">Função isequalobject</span><span class="sxs-lookup"><span data-stu-id="b2c41-103">IsEqualObject function</span></span>

<span data-ttu-id="b2c41-104">A `IsEqualObject` função verifica se duas interfaces estão no mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="b2c41-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2c41-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="b2c41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2c41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c41-107">*pFirst*</span><span class="sxs-lookup"><span data-stu-id="b2c41-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c41-108">Ponteiro para uma interface.</span><span class="sxs-lookup"><span data-stu-id="b2c41-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="b2c41-109">*pSecond*</span><span class="sxs-lookup"><span data-stu-id="b2c41-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c41-110">Ponteiro para a outra interface.</span><span class="sxs-lookup"><span data-stu-id="b2c41-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c41-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2c41-111">Return value</span></span>

<span data-ttu-id="b2c41-112">Retornará **true** se as interfaces estiverem no mesmo objeto ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b2c41-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c41-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2c41-113">Requirements</span></span>



| <span data-ttu-id="b2c41-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2c41-114">Requirement</span></span> | <span data-ttu-id="b2c41-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b2c41-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c41-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2c41-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b2c41-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2c41-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b2c41-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2c41-118">Library</span></span><br/> | <dl> <span data-ttu-id="b2c41-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b2c41-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c41-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2c41-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c41-121">Funções auxiliares diversas</span><span class="sxs-lookup"><span data-stu-id="b2c41-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




