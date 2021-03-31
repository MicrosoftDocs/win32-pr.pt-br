---
title: atributo opcional
description: O atributo \ optional \ especifica um parâmetro opcional para uma função de membro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- atributo opcional MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823752"
---
# <a name="optional-attribute"></a><span data-ttu-id="bc806-104">atributo opcional</span><span class="sxs-lookup"><span data-stu-id="bc806-104">optional attribute</span></span>

<span data-ttu-id="bc806-105">O atributo **\[ opcional \]** especifica um parâmetro opcional para uma função de membro.</span><span class="sxs-lookup"><span data-stu-id="bc806-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="bc806-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc806-107">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="bc806-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-108">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="bc806-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-109">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="bc806-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-110">Especifica o nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="bc806-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-111">*outros atributos*</span><span class="sxs-lookup"><span data-stu-id="bc806-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-112">Zero ou mais atributos MIDL opcionais.</span><span class="sxs-lookup"><span data-stu-id="bc806-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-113">*tipo de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="bc806-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-114">O tipo de dados do parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="bc806-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-115">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="bc806-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-116">Especifica o nome do parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="bc806-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc806-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc806-117">Remarks</span></span>

<span data-ttu-id="bc806-118">O atributo **\[ opcional \]** será válido somente se o parâmetro for do tipo **Variant** ou **Variant** Â \* .</span><span class="sxs-lookup"><span data-stu-id="bc806-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="bc806-119">O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):</span><span class="sxs-lookup"><span data-stu-id="bc806-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="bc806-120">Parâmetros necessários (parâmetros que não têm os atributos **\[** [**DefaultValue**](defaultvalue.md) **\]** ou **\[ optional \]** ),</span><span class="sxs-lookup"><span data-stu-id="bc806-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="bc806-121">Parâmetros opcionais com ou sem o **\[** [](defaultvalue.md) **\]** atributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="bc806-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="bc806-122">Parâmetros com o atributo **\[ opcional \]** e sem o **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** ,</span><span class="sxs-lookup"><span data-stu-id="bc806-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="bc806-123">**\[** parâmetro [**LCID**](lcid.md) **\]** , se houver,</span><span class="sxs-lookup"><span data-stu-id="bc806-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="bc806-124">**\[**[**retval**](retval.md) **\]** meter</span><span class="sxs-lookup"><span data-stu-id="bc806-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="bc806-125">Você não pode aplicar o atributo **\[ opcional \]** a um parâmetro que também tenha os **\[** atributos [**LCID**](lcid.md) **\]** ou **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bc806-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="bc806-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc806-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="bc806-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc806-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc806-128">**ValorPadrão**</span><span class="sxs-lookup"><span data-stu-id="bc806-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="bc806-129">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="bc806-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="bc806-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="bc806-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="bc806-131">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="bc806-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="bc806-132">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="bc806-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="bc806-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="bc806-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 