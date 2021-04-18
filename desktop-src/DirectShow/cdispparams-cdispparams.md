---
description: Método de construtor.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Construtor CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810256"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="8121e-103">Construtor CDispParams. CDispParams</span><span class="sxs-lookup"><span data-stu-id="8121e-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="8121e-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="8121e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8121e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8121e-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="8121e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8121e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8121e-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="8121e-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="8121e-108">Número de argumentos passados para o método ou a propriedade.</span><span class="sxs-lookup"><span data-stu-id="8121e-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="8121e-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="8121e-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="8121e-110">Ponteiro para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="8121e-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="8121e-111">Na lista, cada argumento é armazenado com seu tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="8121e-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8121e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8121e-112">Requirements</span></span>



| <span data-ttu-id="8121e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8121e-113">Requirement</span></span> | <span data-ttu-id="8121e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8121e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8121e-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8121e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8121e-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8121e-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8121e-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8121e-117">Library</span></span><br/> | <dl> <span data-ttu-id="8121e-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8121e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8121e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8121e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8121e-120">**Classe CDispParams**</span><span class="sxs-lookup"><span data-stu-id="8121e-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




