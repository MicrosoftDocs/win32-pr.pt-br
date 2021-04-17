---
description: A macro de observação envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Observação (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757876"
---
# <a name="note"></a><span data-ttu-id="d4dcb-104">OBSERVAÇÃO</span><span class="sxs-lookup"><span data-stu-id="d4dcb-104">NOTE</span></span>

<span data-ttu-id="d4dcb-105">A `NOTE` macro envia uma cadeia de caracteres para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="d4dcb-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="d4dcb-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="d4dcb-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="d4dcb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4dcb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4dcb-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span><span class="sxs-lookup"><span data-stu-id="d4dcb-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="d4dcb-109">Uma cadeia de caracteres de formato de estilo printf.</span><span class="sxs-lookup"><span data-stu-id="d4dcb-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="d4dcb-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span><span class="sxs-lookup"><span data-stu-id="d4dcb-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="d4dcb-111">Argumentos adicionais para a cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="d4dcb-111">Additional arguments for the format string.</span></span> <span data-ttu-id="d4dcb-112">O número de argumentos deve corresponder ao nome da macro.</span><span class="sxs-lookup"><span data-stu-id="d4dcb-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="d4dcb-113">Por exemplo, **NOTE1** usa um argumento e **NOTE5** usa cinco argumentos.</span><span class="sxs-lookup"><span data-stu-id="d4dcb-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4dcb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4dcb-114">Remarks</span></span>

<span data-ttu-id="d4dcb-115">Essas macros são variantes da macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="d4dcb-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="d4dcb-116">Eles geram mensagens de rastreamento de LOG de nível 5 \_ .</span><span class="sxs-lookup"><span data-stu-id="d4dcb-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="d4dcb-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d4dcb-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="d4dcb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4dcb-118">Requirements</span></span>



| <span data-ttu-id="d4dcb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4dcb-119">Requirement</span></span> | <span data-ttu-id="d4dcb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d4dcb-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4dcb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4dcb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d4dcb-122"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4dcb-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4dcb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4dcb-123">Library</span></span><br/> | <dl> <span data-ttu-id="d4dcb-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d4dcb-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4dcb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4dcb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4dcb-126">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="d4dcb-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




