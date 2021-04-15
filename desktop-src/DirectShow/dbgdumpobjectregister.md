---
description: A função DbgDumpObjectRegister exibe informações sobre objetos ativos. Ignorado em compilações de varejo.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Função DbgDumpObjectRegister (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747369"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="f9832-104">Função DbgDumpObjectRegister</span><span class="sxs-lookup"><span data-stu-id="f9832-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="f9832-105">A `DbgDumpObjectRegister` função exibe informações sobre objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="f9832-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="f9832-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="f9832-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9832-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9832-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="f9832-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9832-108">Parameters</span></span>

<span data-ttu-id="f9832-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f9832-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9832-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9832-110">Return value</span></span>

<span data-ttu-id="f9832-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f9832-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9832-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9832-112">Remarks</span></span>

<span data-ttu-id="f9832-113">Em compilações de depuração, a biblioteca de depuração mantém uma lista de objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="f9832-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="f9832-114">A lista inclui todos os objetos que derivam de [**CBaseObject**](cbaseobject.md), foram criados pelo módulo atual e não foram destruídos.</span><span class="sxs-lookup"><span data-stu-id="f9832-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="f9832-115">O construtor **CBaseObject** e os métodos do destruidor atualizam a lista.</span><span class="sxs-lookup"><span data-stu-id="f9832-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="f9832-116">Essa função gera várias mensagens de memória de LOG \_ .</span><span class="sxs-lookup"><span data-stu-id="f9832-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="f9832-117">No nível de log 1, a função exibe apenas o número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="f9832-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="f9832-118">No nível de log 2 ou superior, ele exibe uma lista dos objetos.</span><span class="sxs-lookup"><span data-stu-id="f9832-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9832-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9832-119">Requirements</span></span>



| <span data-ttu-id="f9832-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9832-120">Requirement</span></span> | <span data-ttu-id="f9832-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f9832-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9832-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9832-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f9832-123"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9832-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9832-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9832-124">Library</span></span><br/> | <dl> <span data-ttu-id="f9832-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f9832-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9832-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9832-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9832-127">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="f9832-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




