---
description: Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for falsa. O texto da expressão, o nome do arquivo de origem e o número da linha são registrados usando a macro DbgLog. Ignorado em compilações de varejo.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757248"
---
# <a name="kassert-macro"></a><span data-ttu-id="92bf7-105">Macro KASSERT</span><span class="sxs-lookup"><span data-stu-id="92bf7-105">KASSERT macro</span></span>

<span data-ttu-id="92bf7-106">Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for **falsa**.</span><span class="sxs-lookup"><span data-stu-id="92bf7-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="92bf7-107">O texto da expressão, o nome do arquivo de origem e o número da linha são registrados usando a macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="92bf7-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="92bf7-108">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="92bf7-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="92bf7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92bf7-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="92bf7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92bf7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bf7-111">*condicional*</span><span class="sxs-lookup"><span data-stu-id="92bf7-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="92bf7-112">Expressão para avaliar.</span><span class="sxs-lookup"><span data-stu-id="92bf7-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bf7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92bf7-113">Return value</span></span>

<span data-ttu-id="92bf7-114">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="92bf7-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92bf7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="92bf7-115">Remarks</span></span>

<span data-ttu-id="92bf7-116">Ao contrário das macros [**Assert e**](assert.md) [**Execute \_ Assert**](execute-assert.md) , essa macro não exibe uma caixa de mensagem solicitando o usuário.</span><span class="sxs-lookup"><span data-stu-id="92bf7-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="92bf7-117">Em compilações de depuração, se a expressão for **false**, a macro automaticamente fará com que uma exceção de ponto de interrupção ocorra.</span><span class="sxs-lookup"><span data-stu-id="92bf7-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="92bf7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bf7-118">Requirements</span></span>



| <span data-ttu-id="92bf7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="92bf7-119">Requirement</span></span> | <span data-ttu-id="92bf7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="92bf7-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92bf7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92bf7-121">Header</span></span><br/> | <dl> <span data-ttu-id="92bf7-122"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92bf7-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92bf7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="92bf7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92bf7-124">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="92bf7-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




