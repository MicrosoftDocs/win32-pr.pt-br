---
title: macro Max (Minwindef. h)
description: A macro Max compara dois valores e retorna o maior. O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Multimídia máxima do Windows de macro
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499326"
---
# <a name="max-macro"></a><span data-ttu-id="99631-106">macro máx</span><span class="sxs-lookup"><span data-stu-id="99631-106">max macro</span></span>

<span data-ttu-id="99631-107">A macro **Max** compara dois valores e retorna o maior.</span><span class="sxs-lookup"><span data-stu-id="99631-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="99631-108">O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados.</span><span class="sxs-lookup"><span data-stu-id="99631-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="99631-109">O tipo de dados dos argumentos e o valor de retorno são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="99631-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="99631-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99631-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="99631-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99631-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99631-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="99631-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="99631-113">Especifica o primeiro de dois valores.</span><span class="sxs-lookup"><span data-stu-id="99631-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="99631-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="99631-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="99631-115">Especifica o segundo de dois valores.</span><span class="sxs-lookup"><span data-stu-id="99631-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99631-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99631-116">Return value</span></span>

<span data-ttu-id="99631-117">O valor de retorno é o maior dos dois valores especificados.</span><span class="sxs-lookup"><span data-stu-id="99631-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="99631-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="99631-118">Remarks</span></span>

<span data-ttu-id="99631-119">A macro **Max** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="99631-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="99631-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99631-120">Requirements</span></span>



| <span data-ttu-id="99631-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="99631-121">Requirement</span></span> | <span data-ttu-id="99631-122">Valor</span><span class="sxs-lookup"><span data-stu-id="99631-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99631-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99631-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99631-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99631-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="99631-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99631-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99631-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99631-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99631-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99631-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99631-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="99631-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





