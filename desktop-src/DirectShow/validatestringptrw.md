---
description: Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres largos. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Macro ValidateStringPtrW (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779225"
---
# <a name="validatestringptrw-macro"></a><span data-ttu-id="c24f0-104">Macro ValidateStringPtrW</span><span class="sxs-lookup"><span data-stu-id="c24f0-104">ValidateStringPtrW macro</span></span>

<span data-ttu-id="c24f0-105">Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="c24f0-105">Verifies that the calling process has read access to a wide-character string.</span></span> <span data-ttu-id="c24f0-106">Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="c24f0-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="c24f0-107">Esta macro foi preterida.</span><span class="sxs-lookup"><span data-stu-id="c24f0-107">This macro is deprecated.</span></span> <span data-ttu-id="c24f0-108">No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="c24f0-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c24f0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c24f0-109">Syntax</span></span>


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="c24f0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c24f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24f0-111">*DTI*</span><span class="sxs-lookup"><span data-stu-id="c24f0-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c24f0-112">Ponteiro para uma cadeia de caracteres largos terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c24f0-112">Pointer to a NULL-terminated wide-character string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24f0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c24f0-113">Return value</span></span>

<span data-ttu-id="c24f0-114">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c24f0-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c24f0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c24f0-115">Remarks</span></span>

<span data-ttu-id="c24f0-116">Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído.</span><span class="sxs-lookup"><span data-stu-id="c24f0-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="c24f0-117">Essa macro pode ter um custo de desempenho significativo.</span><span class="sxs-lookup"><span data-stu-id="c24f0-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="c24f0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c24f0-118">Requirements</span></span>



| <span data-ttu-id="c24f0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c24f0-119">Requirement</span></span> | <span data-ttu-id="c24f0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c24f0-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c24f0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c24f0-121">Header</span></span><br/> | <dl> <span data-ttu-id="c24f0-122"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c24f0-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c24f0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c24f0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24f0-124">Macros de validação de ponteiro</span><span class="sxs-lookup"><span data-stu-id="c24f0-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




