---
title: atributo padrão
description: O atributo \ default \ indica que a interface ou dispinterface, definida em uma coclass, representa a interface de programação padrão. Esse atributo destina-se a uso por linguagens de macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- atributo padrão MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453997"
---
# <a name="default-attribute"></a><span data-ttu-id="f7cc8-105">atributo padrão</span><span class="sxs-lookup"><span data-stu-id="f7cc8-105">default attribute</span></span>

<span data-ttu-id="f7cc8-106">O atributo **\[ \] padrão** indica que a [**interface**](interface.md) ou [**dispinterface**](dispinterface.md), definida em uma [**coclass**](coclass.md), representa a interface de programação padrão.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="f7cc8-107">Esse atributo destina-se a uso por linguagens de macro.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="f7cc8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7cc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7cc8-109">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="f7cc8-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="f7cc8-110">Especifica um número de identificação universalmente exclusivo para a [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="f7cc8-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7cc8-111">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="f7cc8-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f7cc8-112">Especifica atributos de [**coclasse**](coclass.md) adicionais.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="f7cc8-113">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f7cc8-114">*coclass-Name*</span><span class="sxs-lookup"><span data-stu-id="f7cc8-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f7cc8-115">Especifica o nome pelo qual outros componentes de software podem fazer referência a essa [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="f7cc8-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7cc8-116">*atributo opcional-interface-*</span><span class="sxs-lookup"><span data-stu-id="f7cc8-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="f7cc8-117">O **\[** atributo de [**origem**](source.md) **\]** , que especifica que uma interface ou dispinterface é de saída, é o único outro atributo que pode ser usado aqui.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="f7cc8-118">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="f7cc8-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f7cc8-119">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7cc8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7cc8-120">Remarks</span></span>

<span data-ttu-id="f7cc8-121">Uma [**coclass**](coclass.md) pode ter no máximo dois membros **\[ padrão \]** .</span><span class="sxs-lookup"><span data-stu-id="f7cc8-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="f7cc8-122">Uma representa a interface de saída (origem) ou a dispinterface, e a outra representa a interface de entrada (coletor) ou a dispinterface.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="f7cc8-123">Se o atributo **\[ padrão \]** não for especificado para nenhum membro da **coclasse** ou **cotipo**, os primeiros membros de saída e de entrada que não têm o atributo **\[** [**restrito**](restricted.md) **\]** serão tratados como os padrões.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="f7cc8-124">Flags</span><span class="sxs-lookup"><span data-stu-id="f7cc8-124">Flags</span></span>

<span data-ttu-id="f7cc8-125">IMPLTYPEFLAG \_ FDEFAULT</span><span class="sxs-lookup"><span data-stu-id="f7cc8-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="f7cc8-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7cc8-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="f7cc8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7cc8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7cc8-128">**coclass**</span><span class="sxs-lookup"><span data-stu-id="f7cc8-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="f7cc8-129">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="f7cc8-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="f7cc8-130">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="f7cc8-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f7cc8-131">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="f7cc8-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f7cc8-132">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="f7cc8-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f7cc8-133">**Restricted**</span><span class="sxs-lookup"><span data-stu-id="f7cc8-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="f7cc8-134">**original**</span><span class="sxs-lookup"><span data-stu-id="f7cc8-134">**source**</span></span>](source.md)
</dt> </dl>

 

 