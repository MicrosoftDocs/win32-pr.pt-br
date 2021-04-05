---
title: atributo propputref
description: O atributo \ propputref \ especifica uma função de configuração de propriedade que usa uma referência em vez de um valor.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref do atributo MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917180"
---
# <a name="propputref-attribute"></a><span data-ttu-id="ac54a-104">atributo propputref</span><span class="sxs-lookup"><span data-stu-id="ac54a-104">propputref attribute</span></span>

<span data-ttu-id="ac54a-105">O atributo **\[ propputref \]** especifica uma função de configuração de propriedade que usa uma referência em vez de um valor.</span><span class="sxs-lookup"><span data-stu-id="ac54a-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="ac54a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac54a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac54a-107">*opcional-atributos de propriedade*</span><span class="sxs-lookup"><span data-stu-id="ac54a-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ac54a-108">Zero ou mais atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ac54a-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="ac54a-109">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="ac54a-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ac54a-110">O tipo dos dados retornados pelo procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="ac54a-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ac54a-111">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="ac54a-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ac54a-112">O nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="ac54a-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ac54a-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="ac54a-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="ac54a-114">Zero ou mais parâmetros para o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="ac54a-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac54a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac54a-115">Remarks</span></span>

<span data-ttu-id="ac54a-116">Uma função que tem o atributo **\[ propputref \]** também deve ter, como seu último parâmetro, um ponteiro que tem o **\[** atributo [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ac54a-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="ac54a-117">A propriedade deve ter o mesmo nome que a função.</span><span class="sxs-lookup"><span data-stu-id="ac54a-117">The property must have the same name as the function.</span></span> <span data-ttu-id="ac54a-118">No máximo, um dos **\[** atributos [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** e **\[ propputref \]** pode ser especificado para uma função.</span><span class="sxs-lookup"><span data-stu-id="ac54a-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="ac54a-119">Flags</span><span class="sxs-lookup"><span data-stu-id="ac54a-119">Flags</span></span>

<span data-ttu-id="ac54a-120">INVOCAr \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="ac54a-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="ac54a-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac54a-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="ac54a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac54a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac54a-123">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="ac54a-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ac54a-124">**no**</span><span class="sxs-lookup"><span data-stu-id="ac54a-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ac54a-125">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="ac54a-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ac54a-126">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="ac54a-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ac54a-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="ac54a-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="ac54a-128">**propput**</span><span class="sxs-lookup"><span data-stu-id="ac54a-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="ac54a-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="ac54a-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 