---
title: atributo HelpString
description: O atributo \ HelpString \ especifica uma cadeia de caracteres que é usada para descrever o elemento ao qual se aplica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- atributo HelpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917193"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="77b8d-104">atributo HelpString</span><span class="sxs-lookup"><span data-stu-id="77b8d-104">helpstring attribute</span></span>

<span data-ttu-id="77b8d-105">O atributo **\[ HelpString \]** especifica uma cadeia de caracteres que é usada para descrever o elemento ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="77b8d-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="77b8d-106">Você pode aplicar o atributo **\[ HelpString \]** às instruções library, importlib, interface, dispinterface, module ou coclass, TYPEDEFs, propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="77b8d-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="77b8d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77b8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b8d-108">*ajuda-texto-cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="77b8d-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="77b8d-109">Uma cadeia de caracteres com terminação zero contendo texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="77b8d-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="77b8d-110">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="77b8d-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="77b8d-111">Zero ou mais instruções de atributo MIDL.</span><span class="sxs-lookup"><span data-stu-id="77b8d-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="77b8d-112">*elementos*</span><span class="sxs-lookup"><span data-stu-id="77b8d-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="77b8d-113">Uma das seguintes diretivas: [**library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="77b8d-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="77b8d-114">*nome do elemento*</span><span class="sxs-lookup"><span data-stu-id="77b8d-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="77b8d-115">O nome que outros componentes de software podem usar para delinear o elemento atual</span><span class="sxs-lookup"><span data-stu-id="77b8d-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="77b8d-116">*defini*</span><span class="sxs-lookup"><span data-stu-id="77b8d-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="77b8d-117">Especifica as instruções que compõem a definição do elemento.</span><span class="sxs-lookup"><span data-stu-id="77b8d-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="77b8d-118">*instrução IDL*</span><span class="sxs-lookup"><span data-stu-id="77b8d-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="77b8d-119">Uma instrução de definição de interface MIDL, como [**propget**](propget.md) ou [**propput**](propput.md).</span><span class="sxs-lookup"><span data-stu-id="77b8d-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77b8d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="77b8d-120">Remarks</span></span>

<span data-ttu-id="77b8d-121">Use as funções [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nas interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) para recuperar a cadeia de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="77b8d-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="77b8d-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77b8d-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="77b8d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="77b8d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b8d-124">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="77b8d-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="77b8d-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="77b8d-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="77b8d-126">**interface**</span><span class="sxs-lookup"><span data-stu-id="77b8d-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="77b8d-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="77b8d-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="77b8d-128">**modulo**</span><span class="sxs-lookup"><span data-stu-id="77b8d-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="77b8d-129">**coclass**</span><span class="sxs-lookup"><span data-stu-id="77b8d-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="77b8d-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="77b8d-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="77b8d-131">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="77b8d-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="77b8d-132">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="77b8d-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="77b8d-133">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="77b8d-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 