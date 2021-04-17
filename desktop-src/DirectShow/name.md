---
description: A macro de nome gera uma cadeia de caracteres somente depuração.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOME (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813084"
---
# <a name="name"></a><span data-ttu-id="bb601-103">NOME</span><span class="sxs-lookup"><span data-stu-id="bb601-103">NAME</span></span>

<span data-ttu-id="bb601-104">A macro de **nome** gera uma cadeia de caracteres somente depuração.</span><span class="sxs-lookup"><span data-stu-id="bb601-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="bb601-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb601-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb601-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="bb601-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="bb601-107">Cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="bb601-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb601-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb601-108">Remarks</span></span>

<span data-ttu-id="bb601-109">Em compilações de depuração, essa macro é equivalente à macro de **texto** .</span><span class="sxs-lookup"><span data-stu-id="bb601-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="bb601-110">Em compilações de varejo, ele é resolvido para (TCHAR \* ) **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bb601-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="bb601-111">Essa macro é útil ao declarar o nome de um objeto que deriva da classe [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bb601-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="bb601-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb601-112">Requirements</span></span>



| <span data-ttu-id="bb601-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb601-113">Requirement</span></span> | <span data-ttu-id="bb601-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bb601-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb601-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb601-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bb601-116"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb601-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb601-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb601-117">Library</span></span><br/> | <dl> <span data-ttu-id="bb601-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bb601-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb601-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb601-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb601-120">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="bb601-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




