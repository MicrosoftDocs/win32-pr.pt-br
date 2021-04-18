---
description: A macro lembrar gera um lembrete no momento da compilação. Essa macro gera uma cadeia de caracteres que inclui a cadeia de caracteres do parâmetro, o nome do arquivo de origem e o número da linha.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: LEMBREte (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779837"
---
# <a name="remind"></a><span data-ttu-id="c6dc1-104">-</span><span class="sxs-lookup"><span data-stu-id="c6dc1-104">REMIND</span></span>

<span data-ttu-id="c6dc1-105">A `REMIND` macro gera um lembrete no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="c6dc1-105">The `REMIND` macro generates a reminder at compile time.</span></span> <span data-ttu-id="c6dc1-106">Essa macro gera uma cadeia de caracteres que inclui a cadeia de caracteres do parâmetro, o nome do arquivo de origem e o número da linha.</span><span class="sxs-lookup"><span data-stu-id="c6dc1-106">This macro generates a string that includes the parameter string, the name of the source file, and the line number.</span></span>

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="c6dc1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6dc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6dc1-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="c6dc1-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="c6dc1-109">Cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="c6dc1-109">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6dc1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6dc1-110">Remarks</span></span>

<span data-ttu-id="c6dc1-111">Essa macro é útil para gerar avisos de tempo de compilação:</span><span class="sxs-lookup"><span data-stu-id="c6dc1-111">This macro is useful for generating compile-time warnings:</span></span>


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a><span data-ttu-id="c6dc1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6dc1-112">Requirements</span></span>



| <span data-ttu-id="c6dc1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6dc1-113">Requirement</span></span> | <span data-ttu-id="c6dc1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c6dc1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dc1-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6dc1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c6dc1-116"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6dc1-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6dc1-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6dc1-117">Library</span></span><br/> | <dl> <span data-ttu-id="c6dc1-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c6dc1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6dc1-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6dc1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6dc1-120">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="c6dc1-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




