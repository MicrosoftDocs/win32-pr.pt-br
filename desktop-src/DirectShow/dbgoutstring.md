---
description: A função DbgOutString envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Função DbgOutString (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747578"
---
# <a name="dbgoutstring-function"></a><span data-ttu-id="5c599-104">Função DbgOutString</span><span class="sxs-lookup"><span data-stu-id="5c599-104">DbgOutString function</span></span>

<span data-ttu-id="5c599-105">A função **DbgOutString** envia uma cadeia de caracteres para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="5c599-105">The **DbgOutString** function sends a string to the debug output location.</span></span> <span data-ttu-id="5c599-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="5c599-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c599-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c599-107">Syntax</span></span>


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a><span data-ttu-id="5c599-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c599-109">*psz*</span><span class="sxs-lookup"><span data-stu-id="5c599-109">*psz*</span></span> 
</dt> <dd>

<span data-ttu-id="5c599-110">Cadeia de caracteres para saída.</span><span class="sxs-lookup"><span data-stu-id="5c599-110">String to output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c599-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c599-111">Return value</span></span>

<span data-ttu-id="5c599-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5c599-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c599-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c599-113">Remarks</span></span>

<span data-ttu-id="5c599-114">Em compilações de depuração, essa função sempre gera a cadeia de caracteres, independentemente dos níveis de saída de depuração atuais.</span><span class="sxs-lookup"><span data-stu-id="5c599-114">In debug builds, this function always outputs the string, regardless of the current debug output levels.</span></span> <span data-ttu-id="5c599-115">Para ter um controle mais preciso sobre a saída, use a macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="5c599-115">For finer control over the output, use the [**DbgLog**](dbglog.md) macro.</span></span>

## <a name="examples"></a><span data-ttu-id="5c599-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c599-116">Examples</span></span>


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a><span data-ttu-id="5c599-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c599-117">Requirements</span></span>



| <span data-ttu-id="5c599-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c599-118">Requirement</span></span> | <span data-ttu-id="5c599-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5c599-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c599-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c599-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5c599-121"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c599-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c599-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c599-122">Library</span></span><br/> | <dl> <span data-ttu-id="5c599-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5c599-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c599-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c599-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c599-125">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="5c599-125">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




