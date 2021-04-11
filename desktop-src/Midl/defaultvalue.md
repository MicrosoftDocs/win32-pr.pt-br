---
title: atributo defaultvalue
description: O atributo \ DefaultValue \ permite que você especifique um valor padrão para um parâmetro opcional tipado.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- atributo DefaultValue de MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294008"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="1dee5-104">atributo defaultvalue</span><span class="sxs-lookup"><span data-stu-id="1dee5-104">defaultvalue attribute</span></span>

<span data-ttu-id="1dee5-105">O atributo **\[ DefaultValue \]** permite que você especifique um valor padrão para um parâmetro opcional tipado.</span><span class="sxs-lookup"><span data-stu-id="1dee5-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="1dee5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dee5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dee5-107">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="1dee5-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-108">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="1dee5-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-109">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="1dee5-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-110">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="1dee5-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-111">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="1dee5-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-112">Especifica o nome da função à qual o atributo **\[ DefaultValue \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="1dee5-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-113">*obrigatório-param-List*</span><span class="sxs-lookup"><span data-stu-id="1dee5-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-114">Especifica um ou mais parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="1dee5-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-115">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="1dee5-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-116">Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1dee5-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-117">*tipo de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="1dee5-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-118">Indica o tipo do parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="1dee5-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-119">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="1dee5-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-120">Especifica o nome do parâmetro opcional.</span><span class="sxs-lookup"><span data-stu-id="1dee5-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1dee5-121">*opcional-lista de parâmetros*</span><span class="sxs-lookup"><span data-stu-id="1dee5-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1dee5-122">Especifica zero ou mais parâmetros adicionais, cada um dos quais deve ter um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1dee5-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dee5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dee5-123">Remarks</span></span>

<span data-ttu-id="1dee5-124">O valor padrão especificado para o parâmetro pode ser qualquer constante ou uma expressão que seja resolvida para uma constante, que pode ser representada por uma **variante**.</span><span class="sxs-lookup"><span data-stu-id="1dee5-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="1dee5-125">Especificamente, você não pode aplicar o atributo **\[ \] DefaultValue** a um parâmetro que é uma estrutura, uma matriz ou um tipo **SafeArray** .</span><span class="sxs-lookup"><span data-stu-id="1dee5-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="1dee5-126">O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):</span><span class="sxs-lookup"><span data-stu-id="1dee5-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="1dee5-127">Parâmetros necessários (parâmetros que não têm os atributos **\[ DefaultValue \]** ou **\[** [**optional**](optional.md) **\]** ),</span><span class="sxs-lookup"><span data-stu-id="1dee5-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="1dee5-128">parâmetros opcionais com ou sem o atributo **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="1dee5-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="1dee5-129">parâmetros com o atributo **\[ opcional \]** e sem o atributo **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="1dee5-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="1dee5-130">**\[** parâmetro [**LCID**](lcid.md) **\]** , se houver,</span><span class="sxs-lookup"><span data-stu-id="1dee5-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="1dee5-131">**\[**[**retval**](retval.md) **\]** meter</span><span class="sxs-lookup"><span data-stu-id="1dee5-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="1dee5-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1dee5-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="1dee5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dee5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dee5-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="1dee5-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="1dee5-135">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="1dee5-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1dee5-136">**interface**</span><span class="sxs-lookup"><span data-stu-id="1dee5-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="1dee5-137">**LCID**</span><span class="sxs-lookup"><span data-stu-id="1dee5-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="1dee5-138">**adicional**</span><span class="sxs-lookup"><span data-stu-id="1dee5-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="1dee5-139">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="1dee5-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="1dee5-140">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="1dee5-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1dee5-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="1dee5-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="1dee5-142">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="1dee5-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 