---
title: atributo dispinterface
description: A instrução dispinterface define um conjunto de propriedades e métodos nos quais você pode chamar a invocação IDispatch.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- MIDL de atributo de dispinterface
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823754"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="10f3e-104">atributo dispinterface</span><span class="sxs-lookup"><span data-stu-id="10f3e-104">dispinterface attribute</span></span>

<span data-ttu-id="10f3e-105">A instrução **dispinterface** define um conjunto de propriedades e métodos nos quais você pode chamar **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="10f3e-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="10f3e-106">Uma dispinterface pode ser definida por meio da listagem explícita do conjunto de métodos e propriedades com suporte (sintaxe 1) ou da listagem de uma única interface (sintaxe 2).</span><span class="sxs-lookup"><span data-stu-id="10f3e-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="10f3e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10f3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f3e-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="10f3e-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="10f3e-109">Especifica os atributos que se aplicam a toda a **dispinterface**.</span><span class="sxs-lookup"><span data-stu-id="10f3e-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="10f3e-110">Os seguintes atributos são aceitos: **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**ArquivoDeAjuda**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**extensível**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="10f3e-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="10f3e-111">*dispinterface-nome*</span><span class="sxs-lookup"><span data-stu-id="10f3e-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="10f3e-112">O nome pelo qual a **dispinterface** é conhecida na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="10f3e-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="10f3e-113">Esse nome deve ser exclusivo na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="10f3e-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="10f3e-114">*lista de propriedades*</span><span class="sxs-lookup"><span data-stu-id="10f3e-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="10f3e-115">(Sintaxe 1) Uma lista opcional de propriedades com suporte pelo objeto, declarada na forma de variáveis.</span><span class="sxs-lookup"><span data-stu-id="10f3e-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="10f3e-116">Essa é a forma abreviada de declarar as funções de propriedade na lista de métodos.</span><span class="sxs-lookup"><span data-stu-id="10f3e-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="10f3e-117">Consulte a seção de comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="10f3e-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="10f3e-118">*lista de métodos*</span><span class="sxs-lookup"><span data-stu-id="10f3e-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="10f3e-119">(Sintaxe 1) Uma lista que inclui um protótipo de função para cada método e Propriedade na **dispinterface**.</span><span class="sxs-lookup"><span data-stu-id="10f3e-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="10f3e-120">Qualquer número de definições de função pode aparecer em *methlist*.</span><span class="sxs-lookup"><span data-stu-id="10f3e-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="10f3e-121">Uma função em *methlist* tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="10f3e-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="10f3e-122">**\[  atributos \]** *ReturnType methname tipo paramName ***(*** params \* \* *);**</span><span class="sxs-lookup"><span data-stu-id="10f3e-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="10f3e-123">Os atributos a seguir são aceitos em um método em uma **dispinterface**: **\[ \] HelpString**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**propputref**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** e **\[** [**vararg**](vararg.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="10f3e-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="10f3e-124">Se **\[ vararg \]** for especificado, o último parâmetro deverá ser uma matriz segura de tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="10f3e-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="10f3e-125">A lista de parâmetros é uma lista delimitada por vírgula, cada elemento do qual tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="10f3e-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="10f3e-126">**\[***atributos***\]**</span><span class="sxs-lookup"><span data-stu-id="10f3e-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="10f3e-127">O *tipo* pode ser qualquer tipo declarado ou interno, ou um ponteiro para qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="10f3e-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="10f3e-128">Os atributos em parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="10f3e-128">Attributes on parameters are:</span></span>

<span data-ttu-id="10f3e-129">**\[**[**entrada**](in.md) **\]** , **\[** [**saída**](out-idl.md) **\]** , **\[** [**opcional**](optional.md) **\]** , **\[ cadeia \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10f3e-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="10f3e-130">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="10f3e-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="10f3e-131">(Sintaxe 2) O nome da interface a ser declarada como uma interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="10f3e-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10f3e-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="10f3e-132">Remarks</span></span>

<span data-ttu-id="10f3e-133">O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):</span><span class="sxs-lookup"><span data-stu-id="10f3e-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="10f3e-134">Parâmetros necessários (parâmetros que não têm os \[ atributos DefaultValue \] ou \[ optional \] ),</span><span class="sxs-lookup"><span data-stu-id="10f3e-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="10f3e-135">parâmetros opcionais com ou sem \[ o \] atributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="10f3e-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="10f3e-136">parâmetros com o \[ \] atributo opcional e sem o \[ \] atributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="10f3e-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="10f3e-137">\[parâmetro [**LCID**](lcid.md) \] , se houver,</span><span class="sxs-lookup"><span data-stu-id="10f3e-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="10f3e-138">\[[**retval**](retval.md) \] meter</span><span class="sxs-lookup"><span data-stu-id="10f3e-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="10f3e-139">As funções de método são especificadas exatamente conforme descrito na página de referência para o [**módulo**](module.md) , exceto pelo fato de que o atributo de \[ [**entrada**](entry.md) \] não é permitido.</span><span class="sxs-lookup"><span data-stu-id="10f3e-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="10f3e-140">Observe que STDOLE32. TLB (STDOLE. O TLB em sistemas de 16 bits) deve ser importado, pois uma **dispinterface** herda de IDispatch.</span><span class="sxs-lookup"><span data-stu-id="10f3e-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="10f3e-141">Você pode declarar Propriedades nas listas Propriedades ou métodos.</span><span class="sxs-lookup"><span data-stu-id="10f3e-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="10f3e-142">A declaração de propriedades na lista de propriedades não indica o tipo de acesso que a propriedade dá suporte (ou seja, Get, PUT ou PUTREF).</span><span class="sxs-lookup"><span data-stu-id="10f3e-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="10f3e-143">Especifique o \[ [](readonly.md) \] atributo ReadOnly para propriedades que não dão suporte a Put ou PUTREF.</span><span class="sxs-lookup"><span data-stu-id="10f3e-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="10f3e-144">Se você declarar as funções de propriedade na lista de métodos, todas as funções de uma propriedade terão o mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="10f3e-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="10f3e-145">Usando a primeira sintaxe, as marcas Properties: and: são obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="10f3e-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="10f3e-146">O \[ atributo [**ID**](id.md) \] também é necessário em cada membro.</span><span class="sxs-lookup"><span data-stu-id="10f3e-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="10f3e-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="10f3e-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="10f3e-148">Diferentemente dos membros da interface, os membros de dispinterface não podem usar o atributo [**retval**](retval.md) para retornar um valor além de um código de erro HRESULT.</span><span class="sxs-lookup"><span data-stu-id="10f3e-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="10f3e-149">O \[ [](lcid.md) \] atributo LCID é, da mesma forma, inválido para dispinterfaces, porque IDispatch:: Invoke passa um LCID.</span><span class="sxs-lookup"><span data-stu-id="10f3e-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="10f3e-150">No entanto, é possível redeclarar uma interface que usa esses atributos.</span><span class="sxs-lookup"><span data-stu-id="10f3e-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="10f3e-151">Usando a segunda sintaxe, as interfaces que dão suporte a IDispatch e são declaradas anteriormente em um script ODL podem ser redeclarados como interfaces IDispatch da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="10f3e-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="10f3e-152">O exemplo anterior declara todos os membros de Hello e todos os membros que Hello herda como suporte a IDispatch.</span><span class="sxs-lookup"><span data-stu-id="10f3e-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="10f3e-153">Nesse caso, se Hello tiver sido declarado anteriormente com \[ \] \[ os membros LCID e retval \] que retornaram HRESULTs, MkTypLib removeria cada \[ \] parâmetro LCID e tipo de retorno HRESULT e, em vez disso, marcaria o tipo de retorno como o do \[ \] parâmetro retval.</span><span class="sxs-lookup"><span data-stu-id="10f3e-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="10f3e-154">A ferramenta de Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="10f3e-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="10f3e-155">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="10f3e-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="10f3e-156">As propriedades e os métodos de uma Dispinterface não fazem parte do VTBL da dispinterface.</span><span class="sxs-lookup"><span data-stu-id="10f3e-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="10f3e-157">Consequentemente, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) e [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) não podem ser usados para implementar IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="10f3e-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="10f3e-158">A dispinterface é usada quando um aplicativo precisa expor funções não VTBL existentes por meio da automação.</span><span class="sxs-lookup"><span data-stu-id="10f3e-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="10f3e-159">Esses aplicativos podem implementar IDispatch:: Invoke examinando o parâmetro dispidMember e chamando diretamente a função correspondente.</span><span class="sxs-lookup"><span data-stu-id="10f3e-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="10f3e-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10f3e-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="10f3e-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="10f3e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f3e-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="10f3e-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="10f3e-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="10f3e-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="10f3e-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="10f3e-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="10f3e-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="10f3e-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="10f3e-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="10f3e-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="10f3e-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="10f3e-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="10f3e-168">**oculto**</span><span class="sxs-lookup"><span data-stu-id="10f3e-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="10f3e-169">**no**</span><span class="sxs-lookup"><span data-stu-id="10f3e-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="10f3e-170">**interface**</span><span class="sxs-lookup"><span data-stu-id="10f3e-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="10f3e-171">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="10f3e-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="10f3e-172">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="10f3e-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="10f3e-173">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="10f3e-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="10f3e-174">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="10f3e-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="10f3e-175">**adicional**</span><span class="sxs-lookup"><span data-stu-id="10f3e-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="10f3e-176">**fora**</span><span class="sxs-lookup"><span data-stu-id="10f3e-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="10f3e-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="10f3e-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="10f3e-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="10f3e-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="10f3e-179">**propput**</span><span class="sxs-lookup"><span data-stu-id="10f3e-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="10f3e-180">**propputref**</span><span class="sxs-lookup"><span data-stu-id="10f3e-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="10f3e-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="10f3e-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="10f3e-182">**Restricted**</span><span class="sxs-lookup"><span data-stu-id="10f3e-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="10f3e-183">**Strings**</span><span class="sxs-lookup"><span data-stu-id="10f3e-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="10f3e-184">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="10f3e-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="10f3e-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="10f3e-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="10f3e-186">**Versão**</span><span class="sxs-lookup"><span data-stu-id="10f3e-186">**version**</span></span>](version.md)
</dt> </dl>

 

 