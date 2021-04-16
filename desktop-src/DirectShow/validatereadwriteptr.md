---
description: Verifica se o processo de chamada tem acesso de leitura/gravação a um bloco de memória. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786962"
---
# <a name="validatereadwriteptr-macro"></a><span data-ttu-id="287d7-104">Macro ValidateReadWritePtr</span><span class="sxs-lookup"><span data-stu-id="287d7-104">ValidateReadWritePtr macro</span></span>

<span data-ttu-id="287d7-105">Verifica se o processo de chamada tem acesso de leitura/gravação a um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="287d7-105">Verifies that the calling process has read/write access to a memory block.</span></span> <span data-ttu-id="287d7-106">Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="287d7-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="287d7-107">Esta macro foi preterida.</span><span class="sxs-lookup"><span data-stu-id="287d7-107">This macro is deprecated.</span></span> <span data-ttu-id="287d7-108">No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="287d7-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="287d7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="287d7-109">Syntax</span></span>


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="287d7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="287d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="287d7-111">*DTI*</span><span class="sxs-lookup"><span data-stu-id="287d7-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="287d7-112">Ponteiro para um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="287d7-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="287d7-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="287d7-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="287d7-114">Tamanho do bloco de memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="287d7-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="287d7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="287d7-115">Return value</span></span>

<span data-ttu-id="287d7-116">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="287d7-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="287d7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="287d7-117">Remarks</span></span>

<span data-ttu-id="287d7-118">Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído.</span><span class="sxs-lookup"><span data-stu-id="287d7-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="287d7-119">Essa macro pode ter um custo de desempenho significativo.</span><span class="sxs-lookup"><span data-stu-id="287d7-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="287d7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="287d7-120">Requirements</span></span>



| <span data-ttu-id="287d7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="287d7-121">Requirement</span></span> | <span data-ttu-id="287d7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="287d7-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="287d7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="287d7-123">Header</span></span><br/> | <dl> <span data-ttu-id="287d7-124"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="287d7-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="287d7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="287d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="287d7-126">Macros de validação de ponteiro</span><span class="sxs-lookup"><span data-stu-id="287d7-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




