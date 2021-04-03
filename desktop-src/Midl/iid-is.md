---
title: Atributo iid_is
description: O atributo \ IID \_ é \ pointer especifica o IID da interface com apontada por um ponteiro de interface.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is do atributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006376"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="721e8-104">IID \_ é atributo</span><span class="sxs-lookup"><span data-stu-id="721e8-104">iid\_is attribute</span></span>

<span data-ttu-id="721e8-105">O **\[ IID \_ é \]** um atributo de ponteiro especifica o IID da interface com apontada por um ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="721e8-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="721e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="721e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="721e8-107">*expressão limitada*</span><span class="sxs-lookup"><span data-stu-id="721e8-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="721e8-108">Especifica uma expressão de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="721e8-108">Specifies a C-language expression.</span></span> <span data-ttu-id="721e8-109">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="721e8-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="721e8-110">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="721e8-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="721e8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="721e8-111">Remarks</span></span>

<span data-ttu-id="721e8-112">Você pode usar o **\[ IID \_ \]** em listas de atributos para parâmetros de função e para membros de estrutura ou União.</span><span class="sxs-lookup"><span data-stu-id="721e8-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="721e8-113">Os stubs usam o IID para determinar como realizar marshaling do ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="721e8-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="721e8-114">Isso é útil para um ponteiro de interface que é digitado como um parâmetro de classe base.</span><span class="sxs-lookup"><span data-stu-id="721e8-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="721e8-115">Os arquivos que usam o **\[ IID \_ é \]** o atributo devem ser compilados com o compilador MIDL no modo padrão, que não está usando a opção [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="721e8-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="721e8-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="721e8-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="721e8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="721e8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721e8-118">**objeto**</span><span class="sxs-lookup"><span data-stu-id="721e8-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="721e8-119">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="721e8-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




