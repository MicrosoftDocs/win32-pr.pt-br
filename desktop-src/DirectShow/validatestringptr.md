---
description: Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug. h)
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
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759896"
---
# <a name="validatestringptr-macro"></a><span data-ttu-id="fe5a6-104">Macro ValidateStringPtr</span><span class="sxs-lookup"><span data-stu-id="fe5a6-104">ValidateStringPtr macro</span></span>

<span data-ttu-id="fe5a6-105">Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-105">Verifies that the calling process has read access to a string.</span></span> <span data-ttu-id="fe5a6-106">Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5a6-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="fe5a6-107">Esta macro foi preterida.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-107">This macro is deprecated.</span></span> <span data-ttu-id="fe5a6-108">No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe5a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe5a6-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="fe5a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe5a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5a6-111">*DTI*</span><span class="sxs-lookup"><span data-stu-id="fe5a6-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="fe5a6-112">Ponteiro para uma cadeia de caracteres **TCHAR** terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-112">Pointer to a NULL-terminated **TCHAR** string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5a6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe5a6-113">Return value</span></span>

<span data-ttu-id="fe5a6-114">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5a6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe5a6-115">Remarks</span></span>

<span data-ttu-id="fe5a6-116">Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="fe5a6-117">Essa macro pode ter um custo de desempenho significativo.</span><span class="sxs-lookup"><span data-stu-id="fe5a6-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe5a6-118">Requirements</span></span>



| <span data-ttu-id="fe5a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe5a6-119">Requirement</span></span> | <span data-ttu-id="fe5a6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fe5a6-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5a6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe5a6-121">Header</span></span><br/> | <dl> <span data-ttu-id="fe5a6-122"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe5a6-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe5a6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe5a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5a6-124">Macros de validação de ponteiro</span><span class="sxs-lookup"><span data-stu-id="fe5a6-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




