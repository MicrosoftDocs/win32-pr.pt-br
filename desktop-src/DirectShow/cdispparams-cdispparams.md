---
description: Construtor de CDispParams. CDispParams-método de construtor.
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
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095784"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="02d40-103">Construtor CDispParams. CDispParams</span><span class="sxs-lookup"><span data-stu-id="02d40-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="02d40-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="02d40-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02d40-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="02d40-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02d40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d40-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="02d40-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="02d40-108">Número de argumentos passados para o método ou a propriedade.</span><span class="sxs-lookup"><span data-stu-id="02d40-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="02d40-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="02d40-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="02d40-110">Ponteiro para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="02d40-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="02d40-111">Na lista, cada argumento é armazenado com seu tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="02d40-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02d40-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02d40-112">Requirements</span></span>



| <span data-ttu-id="02d40-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d40-113">Requirement</span></span> | <span data-ttu-id="02d40-114">Valor</span><span class="sxs-lookup"><span data-stu-id="02d40-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d40-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02d40-115">Header</span></span><br/>  | <dl> <span data-ttu-id="02d40-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02d40-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02d40-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02d40-117">Library</span></span><br/> | <dl> <span data-ttu-id="02d40-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="02d40-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d40-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="02d40-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d40-120">**Classe CDispParams**</span><span class="sxs-lookup"><span data-stu-id="02d40-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




