---
title: atributo personalizado
description: O atributo \ custom \ cria um atributo definido pelo usuário.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- atributo personalizado MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105768735"
---
# <a name="custom-attribute"></a><span data-ttu-id="6c084-104">atributo personalizado</span><span class="sxs-lookup"><span data-stu-id="6c084-104">custom attribute</span></span>

<span data-ttu-id="6c084-105">O atributo **\[ personalizado \]** cria um atributo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6c084-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="6c084-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c084-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c084-107">*ID do atributo*</span><span class="sxs-lookup"><span data-stu-id="6c084-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="6c084-108">O GUID do atributo personalizado.</span><span class="sxs-lookup"><span data-stu-id="6c084-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="6c084-109">*atributo-valor*</span><span class="sxs-lookup"><span data-stu-id="6c084-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="6c084-110">O valor que o atributo mantém.</span><span class="sxs-lookup"><span data-stu-id="6c084-110">The value that the attribute holds.</span></span> <span data-ttu-id="6c084-111">O valor deve ser um que possa ser colocado em um tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="6c084-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="6c084-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="6c084-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6c084-113">Outros atributos, como **\[** [**UUID**](uuid.md) **\]** e **\[** [**HelpString**](helpstring.md) **\]** , que se aplicam a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="6c084-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="6c084-114">*tipo de elemento*</span><span class="sxs-lookup"><span data-stu-id="6c084-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="6c084-115">O tipo de elemento ao qual o atributo personalizado se aplica.</span><span class="sxs-lookup"><span data-stu-id="6c084-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="6c084-116">Isso pode ser uma instrução de biblioteca, informações de tipo, uma variável, uma função ou um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6c084-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="6c084-117">Você não pode usar um atributo personalizado em um membro de uma coclass.</span><span class="sxs-lookup"><span data-stu-id="6c084-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="6c084-118">*nome do elemento*</span><span class="sxs-lookup"><span data-stu-id="6c084-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6c084-119">O nome do elemento.</span><span class="sxs-lookup"><span data-stu-id="6c084-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c084-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c084-120">Remarks</span></span>

<span data-ttu-id="6c084-121">Use o atributo **\[ personalizado \]** para definir seu próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="6c084-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="6c084-122">Por exemplo, você pode criar um atributo com valor de cadeia de caracteres que forneça a ProgID para uma classe.</span><span class="sxs-lookup"><span data-stu-id="6c084-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="6c084-123">Para recuperar um valor de atributo personalizado, chame um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6c084-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="6c084-124">ITypeLib2::GetCustData(rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="6c084-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="6c084-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="6c084-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="6c084-126">ITypeInfo2:: GetFuncCustData (index, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="6c084-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="6c084-127">ITypeInfo2:: GetVarCustData (index, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="6c084-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="6c084-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="6c084-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="6c084-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c084-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c084-130">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="6c084-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="6c084-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="6c084-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="6c084-132">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="6c084-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="6c084-133">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="6c084-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6c084-134">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="6c084-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6c084-135">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="6c084-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 