---
description: Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres ANSI. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Macro ValidateStringPtrA (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759527"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="124ad-104">Macro ValidateStringPtrA</span><span class="sxs-lookup"><span data-stu-id="124ad-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="124ad-105">Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="124ad-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="124ad-106">Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="124ad-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="124ad-107">Esta macro foi preterida.</span><span class="sxs-lookup"><span data-stu-id="124ad-107">This macro is deprecated.</span></span> <span data-ttu-id="124ad-108">No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="124ad-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="124ad-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="124ad-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="124ad-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="124ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124ad-111">*DTI*</span><span class="sxs-lookup"><span data-stu-id="124ad-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="124ad-112">Ponteiro para uma cadeia de caracteres ANSI terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="124ad-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124ad-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="124ad-113">Return value</span></span>

<span data-ttu-id="124ad-114">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="124ad-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="124ad-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="124ad-115">Remarks</span></span>

<span data-ttu-id="124ad-116">Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído.</span><span class="sxs-lookup"><span data-stu-id="124ad-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="124ad-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="124ad-117">Requirements</span></span>



| <span data-ttu-id="124ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="124ad-118">Requirement</span></span> | <span data-ttu-id="124ad-119">Valor</span><span class="sxs-lookup"><span data-stu-id="124ad-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="124ad-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="124ad-120">Header</span></span><br/> | <dl> <span data-ttu-id="124ad-121"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="124ad-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="124ad-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="124ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124ad-123">Macros de validação de ponteiro</span><span class="sxs-lookup"><span data-stu-id="124ad-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




