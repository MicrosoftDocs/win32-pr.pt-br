---
title: atributo immediatebind
description: O atributo \ immediatebind \ indica que o banco de dados será notificado imediatamente de todas as alterações em uma propriedade de um objeto associado a um dado.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind do atributo MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161877"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="e85a0-104">atributo immediatebind</span><span class="sxs-lookup"><span data-stu-id="e85a0-104">immediatebind attribute</span></span>

<span data-ttu-id="e85a0-105">O atributo **\[ immediatebind \]** indica que o banco de dados será notificado imediatamente de todas as alterações a uma propriedade de um objeto associado a um dado.</span><span class="sxs-lookup"><span data-stu-id="e85a0-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="e85a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e85a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e85a0-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="e85a0-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e85a0-108">Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="e85a0-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="e85a0-109">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="e85a0-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e85a0-110">Especifica o nome da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="e85a0-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="e85a0-111">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="e85a0-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e85a0-112">Zero ou mais atributos de função.</span><span class="sxs-lookup"><span data-stu-id="e85a0-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e85a0-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="e85a0-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="e85a0-114">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="e85a0-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e85a0-115">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="e85a0-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e85a0-116">Especifica o nome da função no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="e85a0-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e85a0-117">*params*</span><span class="sxs-lookup"><span data-stu-id="e85a0-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="e85a0-118">Zero ou mais parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="e85a0-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e85a0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e85a0-119">Remarks</span></span>

<span data-ttu-id="e85a0-120">O atributo **\[ immediatebind \]** permite que os controles diferenciem as propriedades que precisam notificar o banco de dados de todas as alterações e as que não têm.</span><span class="sxs-lookup"><span data-stu-id="e85a0-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="e85a0-121">Por exemplo, cada alteração em um controle de caixa de seleção deve ser enviada imediatamente ao banco de dados subjacente, mesmo que o controle não tenha perdido o foco.</span><span class="sxs-lookup"><span data-stu-id="e85a0-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="e85a0-122">No entanto, para um controle ListBox, uma alteração ocorre sempre que uma seleção diferente é realçada.</span><span class="sxs-lookup"><span data-stu-id="e85a0-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="e85a0-123">Notificar o banco de dados de uma alteração antes que o controle perca o foco seria ineficiente e desnecessário.</span><span class="sxs-lookup"><span data-stu-id="e85a0-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="e85a0-124">O atributo **\[ immediatebind \]** permite que você especifique, definindo o bit immediatebind, as propriedades individuais em um formulário cujas alterações devem ser relatadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e85a0-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="e85a0-125">As propriedades que têm o atributo **\[ immediatebind \]** também devem ter o **\[** atributo [**acoplável**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e85a0-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="e85a0-126">Flags</span><span class="sxs-lookup"><span data-stu-id="e85a0-126">Flags</span></span>

<span data-ttu-id="e85a0-127">FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND</span><span class="sxs-lookup"><span data-stu-id="e85a0-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="e85a0-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e85a0-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="e85a0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e85a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85a0-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="e85a0-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="e85a0-131">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="e85a0-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="e85a0-132">**interface**</span><span class="sxs-lookup"><span data-stu-id="e85a0-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="e85a0-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="e85a0-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="e85a0-134">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="e85a0-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e85a0-135">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="e85a0-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e85a0-136">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="e85a0-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 