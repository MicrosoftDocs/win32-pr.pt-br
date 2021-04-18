---
title: atributo de biblioteca
description: A instrução Library contém todas as informações que o compilador MIDL usa para gerar uma biblioteca de tipos.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- atributo de biblioteca MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105753460"
---
# <a name="library-attribute"></a><span data-ttu-id="2a009-104">atributo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a009-104">library attribute</span></span>

<span data-ttu-id="2a009-105">A instrução **library** contém todas as informações que o compilador MIDL usa para gerar uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="2a009-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="2a009-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a009-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a009-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="2a009-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="2a009-108">Especifica um número de identificação universalmente exclusivo para a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2a009-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="2a009-109">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="2a009-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2a009-110">Especifica atributos adicionais que se aplicam a toda a instrução da **biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="2a009-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="2a009-111">Os atributos permitidos incluem **\[** [**controle**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** e **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2a009-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="2a009-112">*nome da biblioteca*</span><span class="sxs-lookup"><span data-stu-id="2a009-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2a009-113">O nome pelo qual os componentes de software se referem à **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="2a009-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="2a009-114">*bibliotecas-definição-instruções*</span><span class="sxs-lookup"><span data-stu-id="2a009-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="2a009-115">Uma ou mais instruções MIDL que definem o conteúdo da **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="2a009-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a009-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a009-116">Remarks</span></span>

<span data-ttu-id="2a009-117">As instruções dentro do bloco de biblioteca podem usar elementos que são declarados dentro ou fora do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2a009-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="2a009-118">As instruções de biblioteca podem usar esses elementos como tipos base, herdando desses elementos ou simplesmente fazendo referência a eles em uma linha, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2a009-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="2a009-119">O compilador MIDL criará uma biblioteca de tipos que inclui definições para cada elemento dentro do bloco de biblioteca, além de definições para quaisquer elementos definidos fora e referenciados de dentro do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2a009-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="2a009-120">Para obter informações sobre como gerar uma biblioteca de tipos e stubs de proxy e cabeçalhos de um único arquivo IDL, consulte [gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span><span class="sxs-lookup"><span data-stu-id="2a009-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2a009-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a009-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="2a009-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a009-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a009-123">Conteúdo de uma biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2a009-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="2a009-124">**controlo**</span><span class="sxs-lookup"><span data-stu-id="2a009-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="2a009-125">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="2a009-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="2a009-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="2a009-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="2a009-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="2a009-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="2a009-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="2a009-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="2a009-129">**oculto**</span><span class="sxs-lookup"><span data-stu-id="2a009-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="2a009-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="2a009-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="2a009-131">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="2a009-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="2a009-132">**Restricted**</span><span class="sxs-lookup"><span data-stu-id="2a009-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="2a009-133">**Versão**</span><span class="sxs-lookup"><span data-stu-id="2a009-133">**version**</span></span>](version.md)
</dt> </dl>

 

 