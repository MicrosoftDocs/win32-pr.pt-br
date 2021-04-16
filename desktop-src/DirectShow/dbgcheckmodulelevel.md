---
description: A função DbgCheckModuleLevel verifica se o log está habilitado para os tipos e o nível de mensagem fornecidos. Ignorado em compilações de varejo.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Função DbgCheckModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758440"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="a12cf-104">Função DbgCheckModuleLevel</span><span class="sxs-lookup"><span data-stu-id="a12cf-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="a12cf-105">A `DbgCheckModuleLevel` função verifica se o log está habilitado para os tipos de mensagem e o nível determinados.</span><span class="sxs-lookup"><span data-stu-id="a12cf-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="a12cf-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="a12cf-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12cf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a12cf-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="a12cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a12cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12cf-109">*Types*</span><span class="sxs-lookup"><span data-stu-id="a12cf-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="a12cf-110">Combinação de bits de um ou mais tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a12cf-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="a12cf-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="a12cf-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="a12cf-112">Nível de log</span><span class="sxs-lookup"><span data-stu-id="a12cf-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12cf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a12cf-113">Return value</span></span>

<span data-ttu-id="a12cf-114">Retornará **true** se o registro em log para qualquer um dos tipos de mensagem especificados for definido como o nível especificado ou superior.</span><span class="sxs-lookup"><span data-stu-id="a12cf-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="a12cf-115">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a12cf-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a12cf-116">Requirements</span></span>



| <span data-ttu-id="a12cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12cf-117">Requirement</span></span> | <span data-ttu-id="a12cf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a12cf-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12cf-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a12cf-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a12cf-120"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a12cf-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a12cf-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a12cf-121">Library</span></span><br/> | <dl> <span data-ttu-id="a12cf-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a12cf-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12cf-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a12cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12cf-124">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="a12cf-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




