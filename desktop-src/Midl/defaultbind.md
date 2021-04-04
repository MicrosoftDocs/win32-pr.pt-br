---
title: atributo defaultbind
description: O atributo \ defaultbind \ indica a propriedade única e vinculável que melhor representa o objeto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- atributo defaultbind MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007521"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="65cd0-104">atributo defaultbind</span><span class="sxs-lookup"><span data-stu-id="65cd0-104">defaultbind attribute</span></span>

<span data-ttu-id="65cd0-105">O atributo **\[ defaultbind \]** indica a propriedade única e vinculável que melhor representa o objeto.</span><span class="sxs-lookup"><span data-stu-id="65cd0-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="65cd0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65cd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65cd0-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="65cd0-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65cd0-108">Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="65cd0-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="65cd0-109">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="65cd0-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="65cd0-110">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="65cd0-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65cd0-111">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="65cd0-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="65cd0-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="65cd0-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="65cd0-113">Especifica uma lista de um ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="65cd0-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="65cd0-114">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="65cd0-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="65cd0-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="65cd0-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="65cd0-116">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="65cd0-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="65cd0-117">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="65cd0-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65cd0-118">Especifica o nome da função à qual o atributo **\[ defaultbind \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="65cd0-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="65cd0-119">*params*</span><span class="sxs-lookup"><span data-stu-id="65cd0-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="65cd0-120">Lista de parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="65cd0-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65cd0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="65cd0-121">Remarks</span></span>

<span data-ttu-id="65cd0-122">As propriedades que têm o atributo **\[ defaultbind \]** também devem ter o **\[** atributo [**acoplável**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="65cd0-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="65cd0-123">Somente uma propriedade em uma interface ou dispinterface pode ter o atributo **\[ defaultbind \]** .</span><span class="sxs-lookup"><span data-stu-id="65cd0-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="65cd0-124">Esse atributo é usado por contêineres que têm um modelo de usuário envolvendo a associação a um objeto em vez de associar a uma propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="65cd0-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="65cd0-125">Um objeto pode dar suporte à ligação de dados, mas não tem esse atributo.</span><span class="sxs-lookup"><span data-stu-id="65cd0-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="65cd0-126">Flags</span><span class="sxs-lookup"><span data-stu-id="65cd0-126">Flags</span></span>

<span data-ttu-id="65cd0-127">FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND</span><span class="sxs-lookup"><span data-stu-id="65cd0-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="65cd0-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65cd0-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="65cd0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="65cd0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65cd0-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="65cd0-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="65cd0-131">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="65cd0-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="65cd0-132">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="65cd0-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="65cd0-133">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="65cd0-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="65cd0-134">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="65cd0-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 