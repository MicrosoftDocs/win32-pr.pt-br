---
description: Verifica se um ponteiro é nulo. Se o ponteiro for nulo, a função ou o método no qual a macro aparece retornará o valor especificado.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro do ponto de verificação (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748200"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="c9d61-104">Macro do ponto de verificação</span><span class="sxs-lookup"><span data-stu-id="c9d61-104">CheckPointer macro</span></span>

<span data-ttu-id="c9d61-105">Verifica se um ponteiro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c9d61-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="c9d61-106">Se o ponteiro for **nulo**, a função ou o método no qual a macro aparece retornará o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c9d61-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d61-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9d61-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="c9d61-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9d61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d61-109">*DTI*</span><span class="sxs-lookup"><span data-stu-id="c9d61-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d61-110">Ponteiro para verificar.</span><span class="sxs-lookup"><span data-stu-id="c9d61-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="c9d61-111">*RET*</span><span class="sxs-lookup"><span data-stu-id="c9d61-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d61-112">Valor que a função ou método retorna se *p* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c9d61-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d61-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9d61-113">Return value</span></span>

<span data-ttu-id="c9d61-114">A função ao redor retornará *RET* se *p* for **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c9d61-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="c9d61-115">Caso contrário, a macro não fará com que a função ao redor seja retornada.</span><span class="sxs-lookup"><span data-stu-id="c9d61-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="c9d61-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9d61-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="c9d61-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9d61-117">Requirements</span></span>



| <span data-ttu-id="c9d61-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d61-118">Requirement</span></span> | <span data-ttu-id="c9d61-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c9d61-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d61-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9d61-120">Header</span></span><br/> | <dl> <span data-ttu-id="c9d61-121"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9d61-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d61-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9d61-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d61-123">Macros de validação de ponteiro</span><span class="sxs-lookup"><span data-stu-id="c9d61-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




