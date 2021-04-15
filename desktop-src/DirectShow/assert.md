---
description: Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for falsa. Ignorado em compilações de varejo.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760779"
---
# <a name="assert-macro"></a><span data-ttu-id="744d6-104">Macro ASSERT</span><span class="sxs-lookup"><span data-stu-id="744d6-104">ASSERT macro</span></span>

<span data-ttu-id="744d6-105">Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for **falsa**.</span><span class="sxs-lookup"><span data-stu-id="744d6-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="744d6-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="744d6-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="744d6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="744d6-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="744d6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="744d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="744d6-109">*condicional*</span><span class="sxs-lookup"><span data-stu-id="744d6-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="744d6-110">Expressão para avaliar.</span><span class="sxs-lookup"><span data-stu-id="744d6-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="744d6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="744d6-111">Return value</span></span>

<span data-ttu-id="744d6-112">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="744d6-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="744d6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="744d6-113">Remarks</span></span>

<span data-ttu-id="744d6-114">Em compilações de depuração, se a expressão for **false**, essa macro exibirá uma caixa de mensagem com o texto da expressão, o nome do arquivo de origem e o número da linha.</span><span class="sxs-lookup"><span data-stu-id="744d6-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="744d6-115">O usuário pode ignorar a asserção, inserir o depurador ou sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="744d6-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="744d6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="744d6-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="744d6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="744d6-117">Requirements</span></span>



| <span data-ttu-id="744d6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="744d6-118">Requirement</span></span> | <span data-ttu-id="744d6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="744d6-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="744d6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="744d6-120">Header</span></span><br/> | <dl> <span data-ttu-id="744d6-121"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="744d6-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744d6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="744d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744d6-123">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="744d6-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




