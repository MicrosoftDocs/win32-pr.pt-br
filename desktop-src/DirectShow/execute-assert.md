---
description: Avalia uma expressão em compilações de depuração e de varejo. Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Macro EXECUTE_ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750637"
---
# <a name="execute_assert-macro"></a><span data-ttu-id="e4f1a-104">EXECUTAR \_ macro Assert</span><span class="sxs-lookup"><span data-stu-id="e4f1a-104">EXECUTE\_ASSERT macro</span></span>

<span data-ttu-id="e4f1a-105">Avalia uma expressão em compilações de depuração e de varejo.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-105">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="e4f1a-106">Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for **false**.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-106">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f1a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4f1a-107">Syntax</span></span>


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="e4f1a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4f1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f1a-109">*condicional*</span><span class="sxs-lookup"><span data-stu-id="e4f1a-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="e4f1a-110">Expressão para avaliar.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f1a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4f1a-111">Return value</span></span>

<span data-ttu-id="e4f1a-112">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4f1a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4f1a-113">Remarks</span></span>

<span data-ttu-id="e4f1a-114">Ao contrário da macro [**Assert**](assert.md) , essa macro avalia a expressão em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-114">Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds.</span></span> <span data-ttu-id="e4f1a-115">Em compilações de depuração, se a expressão for **false**, a macro exibirá uma caixa de mensagem com o texto da expressão, o nome do arquivo de origem e o número da linha.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-115">In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="e4f1a-116">O usuário pode ignorar a asserção, inserir o depurador ou sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-116">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f1a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4f1a-117">Requirements</span></span>



| <span data-ttu-id="e4f1a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f1a-118">Requirement</span></span> | <span data-ttu-id="e4f1a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e4f1a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f1a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4f1a-120">Header</span></span><br/> | <dl> <span data-ttu-id="e4f1a-121"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4f1a-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f1a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4f1a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f1a-123">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="e4f1a-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




