---
title: atributo helpcontext
description: O atributo \ HelpContext \ especifica um identificador de contexto que permite ao usuário exibir informações sobre esse elemento no arquivo de ajuda.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- atributo HelpContext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917206"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="70377-104">atributo helpcontext</span><span class="sxs-lookup"><span data-stu-id="70377-104">helpcontext attribute</span></span>

<span data-ttu-id="70377-105">O \[  \] atributo HelpContext especifica um identificador de contexto que permite ao usuário exibir informações sobre esse elemento no arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="70377-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="70377-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70377-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="70377-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="70377-108">Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**typedef**](typedef.md), **métodos**, **\[ propriedade \]** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="70377-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="70377-109">*HelpContext-Value*</span><span class="sxs-lookup"><span data-stu-id="70377-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="70377-110">Um inteiro exclusivo que identifica o texto de ajuda associado ao elemento MIDL atual.</span><span class="sxs-lookup"><span data-stu-id="70377-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="70377-111">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="70377-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="70377-112">Especifica uma lista de um ou mais atributos que se aplicam ao elemento MIDL como um todo.</span><span class="sxs-lookup"><span data-stu-id="70377-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="70377-113">*elementos*</span><span class="sxs-lookup"><span data-stu-id="70377-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="70377-114">Uma das seguintes diretivas: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="70377-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="70377-115">*nome do elemento*</span><span class="sxs-lookup"><span data-stu-id="70377-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="70377-116">O nome que outros componentes de software podem usar para delinear o elemento atual.</span><span class="sxs-lookup"><span data-stu-id="70377-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="70377-117">*definições*</span><span class="sxs-lookup"><span data-stu-id="70377-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="70377-118">Especifica as instruções que compõem a definição do elemento.</span><span class="sxs-lookup"><span data-stu-id="70377-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70377-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="70377-119">Remarks</span></span>

<span data-ttu-id="70377-120">O \[ **atributo HelpContext** \] pode ser aplicado aos seguintes elementos: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="70377-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="70377-121">O *HelpContext-Value* é um identificador de contexto de 32 bits dentro do arquivo de ajuda que pode ser recuperado com as funções [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nas interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .</span><span class="sxs-lookup"><span data-stu-id="70377-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="70377-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70377-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="70377-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="70377-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70377-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="70377-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="70377-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="70377-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="70377-126">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="70377-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="70377-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="70377-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="70377-128">**interface**</span><span class="sxs-lookup"><span data-stu-id="70377-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="70377-129">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="70377-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="70377-130">**modulo**</span><span class="sxs-lookup"><span data-stu-id="70377-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="70377-131">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="70377-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="70377-132">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="70377-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="70377-133">**typedef**</span><span class="sxs-lookup"><span data-stu-id="70377-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 