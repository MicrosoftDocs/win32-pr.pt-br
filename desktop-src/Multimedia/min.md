---
title: macro min (Minwindef. h)
description: A macro min compara dois valores e retorna o menor. O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Multimídia mín. de macro do Windows
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645256"
---
# <a name="min-macro"></a><span data-ttu-id="6740a-106">macro mín</span><span class="sxs-lookup"><span data-stu-id="6740a-106">min macro</span></span>

<span data-ttu-id="6740a-107">A macro **min** compara dois valores e retorna o menor.</span><span class="sxs-lookup"><span data-stu-id="6740a-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="6740a-108">O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados.</span><span class="sxs-lookup"><span data-stu-id="6740a-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="6740a-109">O tipo de dados dos argumentos e o valor de retorno são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="6740a-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="6740a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6740a-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="6740a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6740a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6740a-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="6740a-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="6740a-113">Especifica o primeiro de dois valores.</span><span class="sxs-lookup"><span data-stu-id="6740a-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="6740a-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="6740a-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="6740a-115">Especifica o segundo de dois valores.</span><span class="sxs-lookup"><span data-stu-id="6740a-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6740a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6740a-116">Return value</span></span>

<span data-ttu-id="6740a-117">O valor de retorno é o menor dos dois valores especificados.</span><span class="sxs-lookup"><span data-stu-id="6740a-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6740a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6740a-118">Remarks</span></span>

<span data-ttu-id="6740a-119">A macro **min** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6740a-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="6740a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6740a-120">Requirements</span></span>



| <span data-ttu-id="6740a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6740a-121">Requirement</span></span> | <span data-ttu-id="6740a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6740a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6740a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6740a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6740a-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6740a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6740a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6740a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6740a-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6740a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6740a-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6740a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6740a-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="6740a-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





