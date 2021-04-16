---
title: atributo oculto
description: O atributo \ Hidden \ indica que o item existe, mas não deve ser exibido em um navegador orientado ao usuário.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- atributo oculto MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105750021"
---
# <a name="hidden-attribute"></a><span data-ttu-id="02bbf-104">atributo oculto</span><span class="sxs-lookup"><span data-stu-id="02bbf-104">hidden attribute</span></span>

<span data-ttu-id="02bbf-105">O atributo **\[ Hidden \]** indica que o item existe, mas não deve ser exibido em um navegador orientado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="02bbf-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="02bbf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bbf-107">*outros atributos*</span><span class="sxs-lookup"><span data-stu-id="02bbf-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-108">Zero ou mais atributos MIDL opcionais.</span><span class="sxs-lookup"><span data-stu-id="02bbf-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="02bbf-109">*elementos*</span><span class="sxs-lookup"><span data-stu-id="02bbf-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-110">Uma das seguintes diretivas: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)ou [**library**](library.md).</span><span class="sxs-lookup"><span data-stu-id="02bbf-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="02bbf-111">*nome do elemento*</span><span class="sxs-lookup"><span data-stu-id="02bbf-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-112">O nome que outros componentes de software podem usar para delinear o elemento atual.</span><span class="sxs-lookup"><span data-stu-id="02bbf-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="02bbf-113">*definições*</span><span class="sxs-lookup"><span data-stu-id="02bbf-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-114">Especifica as instruções que compõem a definição do elemento.</span><span class="sxs-lookup"><span data-stu-id="02bbf-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="02bbf-115">*tipo de função*</span><span class="sxs-lookup"><span data-stu-id="02bbf-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-116">Tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="02bbf-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="02bbf-117">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="02bbf-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-118">Nome usado para invocar a função.</span><span class="sxs-lookup"><span data-stu-id="02bbf-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="02bbf-119">*opcional-lista de parâmetros*</span><span class="sxs-lookup"><span data-stu-id="02bbf-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02bbf-120">Zero ou mais parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="02bbf-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02bbf-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="02bbf-121">Remarks</span></span>

<span data-ttu-id="02bbf-122">O atributo **\[ Hidden \]** permite remover membros de sua interface (blindando-os de uso adicional) enquanto mantém a compatibilidade com o código existente.</span><span class="sxs-lookup"><span data-stu-id="02bbf-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="02bbf-123">Você pode usar o atributo **\[ \] Hidden** em Propriedades, métodos e as instruções [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)e [**library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="02bbf-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="02bbf-124">Quando especificado para uma biblioteca, o atributo **\[ Hidden \]** impede que toda a biblioteca seja exibida.</span><span class="sxs-lookup"><span data-stu-id="02bbf-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="02bbf-125">Esse uso destina-se ao uso com controles.</span><span class="sxs-lookup"><span data-stu-id="02bbf-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="02bbf-126">Os hosts precisam criar uma nova biblioteca de tipos que encapsula o controle com propriedades estendidas.</span><span class="sxs-lookup"><span data-stu-id="02bbf-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="02bbf-127">Flags</span><span class="sxs-lookup"><span data-stu-id="02bbf-127">Flags</span></span>

<span data-ttu-id="02bbf-128">VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN</span><span class="sxs-lookup"><span data-stu-id="02bbf-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="02bbf-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02bbf-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="02bbf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="02bbf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02bbf-131">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="02bbf-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="02bbf-132">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="02bbf-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="02bbf-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="02bbf-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="02bbf-134">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="02bbf-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="02bbf-135">**interface**</span><span class="sxs-lookup"><span data-stu-id="02bbf-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="02bbf-136">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="02bbf-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="02bbf-137">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="02bbf-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="02bbf-138">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="02bbf-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 