---
description: Testa se um ponteiro está alinhado a um limite especificado. Caso contrário, essa macro invoca a macro ASSERT. Ignorado em compilações de varejo.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782201"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="d98e7-105">Macro DbgAssertAligned</span><span class="sxs-lookup"><span data-stu-id="d98e7-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="d98e7-106">Testa se um ponteiro está alinhado a um limite especificado.</span><span class="sxs-lookup"><span data-stu-id="d98e7-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="d98e7-107">Caso contrário, essa macro invoca a macro [**Assert**](assert.md) .</span><span class="sxs-lookup"><span data-stu-id="d98e7-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="d98e7-108">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="d98e7-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98e7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d98e7-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="d98e7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d98e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98e7-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="d98e7-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="d98e7-112">Variável de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="d98e7-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="d98e7-113">*sintonia*</span><span class="sxs-lookup"><span data-stu-id="d98e7-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="d98e7-114">Alinhamento necessário.</span><span class="sxs-lookup"><span data-stu-id="d98e7-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98e7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d98e7-115">Return value</span></span>

<span data-ttu-id="d98e7-116">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d98e7-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d98e7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d98e7-117">Requirements</span></span>



| <span data-ttu-id="d98e7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98e7-118">Requirement</span></span> | <span data-ttu-id="d98e7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d98e7-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98e7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d98e7-120">Header</span></span><br/> | <dl> <span data-ttu-id="d98e7-121"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d98e7-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98e7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d98e7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98e7-123">Macros Assert e Breakpoint</span><span class="sxs-lookup"><span data-stu-id="d98e7-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




