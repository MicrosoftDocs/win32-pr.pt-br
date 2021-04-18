---
description: Verifica se o processo de chamada tem acesso de leitura a um bloco de memória. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787124"
---
# <a name="validatereadptr-macro"></a><span data-ttu-id="ff019-104">Macro ValidateReadPtr</span><span class="sxs-lookup"><span data-stu-id="ff019-104">ValidateReadPtr macro</span></span>

<span data-ttu-id="ff019-105">Verifica se o processo de chamada tem acesso de leitura a um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="ff019-105">Verifies that the calling process has read access to a memory block.</span></span> <span data-ttu-id="ff019-106">Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="ff019-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="ff019-107">Esta macro foi preterida.</span><span class="sxs-lookup"><span data-stu-id="ff019-107">This macro is deprecated.</span></span> <span data-ttu-id="ff019-108">No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="ff019-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ff019-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff019-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="ff019-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff019-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff019-111">*DTI*</span><span class="sxs-lookup"><span data-stu-id="ff019-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="ff019-112">Ponteiro para um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="ff019-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="ff019-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="ff019-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="ff019-114">Tamanho do bloco de memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ff019-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff019-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff019-115">Return value</span></span>

<span data-ttu-id="ff019-116">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ff019-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff019-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff019-117">Remarks</span></span>

<span data-ttu-id="ff019-118">Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído.</span><span class="sxs-lookup"><span data-stu-id="ff019-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="ff019-119">Essa macro pode ter um custo de desempenho significativo.</span><span class="sxs-lookup"><span data-stu-id="ff019-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff019-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff019-120">Requirements</span></span>



| <span data-ttu-id="ff019-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff019-121">Requirement</span></span> | <span data-ttu-id="ff019-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ff019-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff019-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff019-123">Header</span></span><br/> | <dl> <span data-ttu-id="ff019-124"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff019-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff019-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff019-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff019-126">Macros de validação de ponteiro</span><span class="sxs-lookup"><span data-stu-id="ff019-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




