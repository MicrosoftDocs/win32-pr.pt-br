---
title: atributo displaybind
description: O atributo \ displaybind \ indica uma propriedade que deve ser exibida para o usuário como vinculável.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- displaybind do atributo MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640633"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="86c90-104">atributo displaybind</span><span class="sxs-lookup"><span data-stu-id="86c90-104">displaybind attribute</span></span>

<span data-ttu-id="86c90-105">O atributo **\[ displaybind \]** indica uma propriedade que deve ser exibida para o usuário como vinculável.</span><span class="sxs-lookup"><span data-stu-id="86c90-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="86c90-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86c90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c90-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="86c90-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="86c90-108">Especifica uma lista opcional de atributos de interface.</span><span class="sxs-lookup"><span data-stu-id="86c90-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="86c90-109">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="86c90-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="86c90-110">O nome da interface.</span><span class="sxs-lookup"><span data-stu-id="86c90-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="86c90-111">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="86c90-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="86c90-112">Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao tipo de retorno de função.</span><span class="sxs-lookup"><span data-stu-id="86c90-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="86c90-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="86c90-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="86c90-114">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="86c90-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="86c90-115">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="86c90-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="86c90-116">Especifica o nome da função à qual o atributo **\[ displaybind \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="86c90-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="86c90-117">*params*</span><span class="sxs-lookup"><span data-stu-id="86c90-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="86c90-118">Lista de parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="86c90-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86c90-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="86c90-119">Remarks</span></span>

<span data-ttu-id="86c90-120">As propriedades que têm o atributo **\[ displaybind \]** também devem ter o **\[** atributo [**acoplável**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="86c90-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="86c90-121">Um objeto pode dar suporte à ligação de dados, mas não tem esse atributo.</span><span class="sxs-lookup"><span data-stu-id="86c90-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="86c90-122">Flags</span><span class="sxs-lookup"><span data-stu-id="86c90-122">Flags</span></span>

<span data-ttu-id="86c90-123">FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND</span><span class="sxs-lookup"><span data-stu-id="86c90-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="86c90-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="86c90-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="86c90-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="86c90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c90-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="86c90-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="86c90-127">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="86c90-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="86c90-128">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="86c90-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="86c90-129">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="86c90-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="86c90-130">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="86c90-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 