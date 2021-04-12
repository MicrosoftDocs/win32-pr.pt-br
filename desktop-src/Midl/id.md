---
title: ID do atributo
description: O atributo \ ID \ especifica um DISPID para uma função membro (uma propriedade ou um método, em uma interface ou Dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- atributo de ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365872"
---
# <a name="id-attribute"></a><span data-ttu-id="4e0b7-104">ID do atributo</span><span class="sxs-lookup"><span data-stu-id="4e0b7-104">id attribute</span></span>

<span data-ttu-id="4e0b7-105">O atributo **\[ ID \]** especifica um DISPID para uma função membro (uma propriedade ou um método, em uma interface ou Dispinterface).</span><span class="sxs-lookup"><span data-stu-id="4e0b7-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="4e0b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e0b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0b7-107">*ID-num*</span><span class="sxs-lookup"><span data-stu-id="4e0b7-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="4e0b7-108">DISPID para a função.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="4e0b7-109">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="4e0b7-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4e0b7-110">Especifica uma lista de zero ou mais atributos de interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4e0b7-111">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="4e0b7-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4e0b7-112">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="4e0b7-113">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="4e0b7-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4e0b7-114">Especifica o nome da função no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="4e0b7-115">*opcional-lista de parâmetros*</span><span class="sxs-lookup"><span data-stu-id="4e0b7-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4e0b7-116">Zero ou mais parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e0b7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e0b7-117">Remarks</span></span>

<span data-ttu-id="4e0b7-118">Use o atributo **\[ \] ID** quando desejar atribuir um DISPID padrão (como o valor DISPID \_ , DISPID \_ NEWENUM etc.) a um método ou propriedade, ou quando você implementar seu próprio **IDispatch:: Invoke** em vez de delegar para o **DispInvoke** / **ITypeInfo:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="4e0b7-119">Se você não usar o atributo **\[ ID \]** em uma interface, o compilador MIDL atribuirá um DISPID para você.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="4e0b7-120">No entanto, ao especificar uma dispinterface usando propriedades e métodos, você deve especificar um DISPID para cada propriedade e método.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="4e0b7-121">O *ID-num* é um valor integral positivo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="4e0b7-122">As IDs negativas são reservadas para uso pela automação.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="4e0b7-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e0b7-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="4e0b7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e0b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0b7-125">**interface**</span><span class="sxs-lookup"><span data-stu-id="4e0b7-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4e0b7-126">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="4e0b7-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="4e0b7-127">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="4e0b7-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4e0b7-128">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="4e0b7-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4e0b7-129">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="4e0b7-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 