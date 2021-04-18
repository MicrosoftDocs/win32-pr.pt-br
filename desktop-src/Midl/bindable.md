---
title: atributo vinculável
description: O atributo \ acoplável \ indica que a propriedade dá suporte à vinculação de dados.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- atributo vinculável MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105789784"
---
# <a name="bindable-attribute"></a><span data-ttu-id="91bf3-104">atributo vinculável</span><span class="sxs-lookup"><span data-stu-id="91bf3-104">bindable attribute</span></span>

<span data-ttu-id="91bf3-105">O atributo **\[ acoplável \]** indica que a propriedade dá suporte à vinculação de dados.</span><span class="sxs-lookup"><span data-stu-id="91bf3-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="91bf3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91bf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91bf3-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="91bf3-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91bf3-108">Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="91bf3-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="91bf3-109">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="91bf3-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="91bf3-110">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="91bf3-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91bf3-111">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="91bf3-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="91bf3-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="91bf3-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91bf3-113">Especifica zero ou mais atributos que se aplicam ao protótipo de função para uma propriedade ou um método em uma [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="91bf3-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="91bf3-114">Os seguintes atributos são válidos: [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)e [**\[ vararg \]**](vararg.md).</span><span class="sxs-lookup"><span data-stu-id="91bf3-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="91bf3-115">Se **vararg** for especificado, o último parâmetro deverá ser uma matriz segura do tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="91bf3-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="91bf3-116">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="91bf3-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="91bf3-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="91bf3-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="91bf3-118">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="91bf3-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="91bf3-119">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="91bf3-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91bf3-120">Especifica o nome da função à qual o atributo **\[ vinculável \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="91bf3-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="91bf3-121">*params*</span><span class="sxs-lookup"><span data-stu-id="91bf3-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="91bf3-122">Lista de parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="91bf3-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91bf3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="91bf3-123">Remarks</span></span>

<span data-ttu-id="91bf3-124">Ao dar suporte à ligação de dados, o atributo **\[ vinculável \]** permite que o cliente seja notificado sempre que uma propriedade tiver alterado o valor.</span><span class="sxs-lookup"><span data-stu-id="91bf3-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="91bf3-125">(Se você quiser que o cliente seja notificado de alterações iminentes em uma propriedade, use o atributo [**\[ requestedit \]**](requestedit.md) .)</span><span class="sxs-lookup"><span data-stu-id="91bf3-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="91bf3-126">Como o atributo **\[ acoplável \]** se refere à propriedade como um todo, ele deve ser especificado onde quer que a propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="91bf3-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="91bf3-127">Portanto, você precisa especificar o atributo na função de acesso à propriedade e na função de configuração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="91bf3-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="91bf3-128">Flags</span><span class="sxs-lookup"><span data-stu-id="91bf3-128">Flags</span></span>

<span data-ttu-id="91bf3-129">FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE</span><span class="sxs-lookup"><span data-stu-id="91bf3-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="91bf3-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91bf3-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="91bf3-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="91bf3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bf3-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="91bf3-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="91bf3-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="91bf3-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="91bf3-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="91bf3-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="91bf3-135">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="91bf3-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="91bf3-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="91bf3-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="91bf3-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="91bf3-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="91bf3-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="91bf3-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="91bf3-139">**interface**</span><span class="sxs-lookup"><span data-stu-id="91bf3-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="91bf3-140">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="91bf3-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="91bf3-141">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="91bf3-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="91bf3-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="91bf3-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="91bf3-143">**propput**</span><span class="sxs-lookup"><span data-stu-id="91bf3-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="91bf3-144">**propputref**</span><span class="sxs-lookup"><span data-stu-id="91bf3-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="91bf3-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="91bf3-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="91bf3-146">**string**</span><span class="sxs-lookup"><span data-stu-id="91bf3-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="91bf3-147">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="91bf3-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="91bf3-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="91bf3-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 