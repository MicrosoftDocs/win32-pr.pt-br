---
description: A macro DbgLog envia uma cadeia de caracteres para o local de saída de depuração, se o registro em log estiver habilitado para o tipo e o nível especificados. Essa macro é ignorada em compilações de varejo.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754216"
---
# <a name="dbglog-macro"></a><span data-ttu-id="10d6e-104">Macro DbgLog</span><span class="sxs-lookup"><span data-stu-id="10d6e-104">DbgLog macro</span></span>

<span data-ttu-id="10d6e-105">A macro **DbgLog** envia uma cadeia de caracteres para o local de saída de depuração, se o registro em log estiver habilitado para o tipo e o nível especificados.</span><span class="sxs-lookup"><span data-stu-id="10d6e-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="10d6e-106">Essa macro é ignorada em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="10d6e-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d6e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10d6e-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="10d6e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10d6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d6e-109">*Types*</span><span class="sxs-lookup"><span data-stu-id="10d6e-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="10d6e-110">Combinação de bits de um ou mais tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="10d6e-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="10d6e-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="10d6e-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="10d6e-112">Nível de log desta mensagem.</span><span class="sxs-lookup"><span data-stu-id="10d6e-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="10d6e-113">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="10d6e-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="10d6e-114">Uma cadeia de caracteres de formato de estilo **printf** .</span><span class="sxs-lookup"><span data-stu-id="10d6e-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="10d6e-115">*...*</span><span class="sxs-lookup"><span data-stu-id="10d6e-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="10d6e-116">Argumentos adicionais para a cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="10d6e-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d6e-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10d6e-117">Return value</span></span>

<span data-ttu-id="10d6e-118">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="10d6e-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d6e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="10d6e-119">Remarks</span></span>

<span data-ttu-id="10d6e-120">Se o log de depuração de qualquer um dos tipos de mensagem for definido como o nível especificado ou superior, essa macro enviará a cadeia de caracteres formatada para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="10d6e-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="10d6e-121">A macro adiciona automaticamente um caractere de nova linha à cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="10d6e-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="10d6e-122">Um conjunto adicional de parênteses deve incluir os parâmetros da macro:</span><span class="sxs-lookup"><span data-stu-id="10d6e-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="10d6e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10d6e-123">Requirements</span></span>



| <span data-ttu-id="10d6e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d6e-124">Requirement</span></span> | <span data-ttu-id="10d6e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="10d6e-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d6e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10d6e-126">Header</span></span><br/> | <dl> <span data-ttu-id="10d6e-127"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10d6e-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d6e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="10d6e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d6e-129">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="10d6e-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




