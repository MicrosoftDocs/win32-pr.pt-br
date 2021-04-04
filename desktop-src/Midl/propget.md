---
title: atributo propget
description: O atributo \ propget \ especifica uma função de acessador de propriedade. A propriedade deve ter o mesmo nome que a função.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- propget do atributo MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007392"
---
# <a name="propget-attribute"></a><span data-ttu-id="e760a-105">atributo propget</span><span class="sxs-lookup"><span data-stu-id="e760a-105">propget attribute</span></span>

<span data-ttu-id="e760a-106">O atributo **\[ propget \]** especifica uma função de acessador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e760a-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="e760a-107">A propriedade deve ter o mesmo nome que a função.</span><span class="sxs-lookup"><span data-stu-id="e760a-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="e760a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e760a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e760a-109">*opcional-atributos de propriedade*</span><span class="sxs-lookup"><span data-stu-id="e760a-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e760a-110">Zero ou mais atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e760a-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e760a-111">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="e760a-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e760a-112">O tipo dos dados retornados pelo procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e760a-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e760a-113">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="e760a-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e760a-114">O nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e760a-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e760a-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="e760a-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="e760a-116">Zero ou mais parâmetros para o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e760a-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e760a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e760a-117">Remarks</span></span>

<span data-ttu-id="e760a-118">Uma função que tem o atributo propget também deve ter, como seu último parâmetro, um tipo de ponteiro com os **\[** atributos [**out**](out-idl.md) **\]** e **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e760a-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="e760a-119">Se o último parâmetro não tiver os \[ atributos de out, retval \] , o valor de retorno da função será tratado como um \[ parâmetro retval out \] .</span><span class="sxs-lookup"><span data-stu-id="e760a-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="e760a-120">Por exemplo, uma função com o protótipo</span><span class="sxs-lookup"><span data-stu-id="e760a-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="e760a-121">é tratado como</span><span class="sxs-lookup"><span data-stu-id="e760a-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="e760a-122">No máximo, um de **\[ propget \]**, **\[** [**propput**](propput.md) **\]** e **\[** [**propputref**](propputref.md) **\]** pode ser especificado para uma função.</span><span class="sxs-lookup"><span data-stu-id="e760a-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="e760a-123">Se o **\[** [](lcid.md) **\]** atributo LCID for usado na lista de parâmetros de uma função que contém um parâmetro com o **\[** atributo [**propput**](propput.md) **\]** , o parâmetro **\[ LCID \]** deverá ser segundo para o último.</span><span class="sxs-lookup"><span data-stu-id="e760a-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="e760a-124">Flags</span><span class="sxs-lookup"><span data-stu-id="e760a-124">Flags</span></span>

<span data-ttu-id="e760a-125">INVOCAr \_ PROPERTYGET</span><span class="sxs-lookup"><span data-stu-id="e760a-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="e760a-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e760a-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="e760a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e760a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e760a-128">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="e760a-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e760a-129">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="e760a-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e760a-130">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="e760a-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e760a-131">**fora**</span><span class="sxs-lookup"><span data-stu-id="e760a-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="e760a-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="e760a-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="e760a-133">**propput**</span><span class="sxs-lookup"><span data-stu-id="e760a-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="e760a-134">**propputref**</span><span class="sxs-lookup"><span data-stu-id="e760a-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="e760a-135">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="e760a-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 