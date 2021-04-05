---
title: atributo dual
description: O atributo Dual identifica uma interface que expõe propriedades e métodos por meio de IDispatch e diretamente por meio de VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL de atributo duplo
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917285"
---
# <a name="dual-attribute"></a><span data-ttu-id="a74af-104">atributo dual</span><span class="sxs-lookup"><span data-stu-id="a74af-104">dual attribute</span></span>

<span data-ttu-id="a74af-105">O atributo **Dual** identifica uma interface que expõe propriedades e métodos por meio de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e diretamente por meio de VTBL.</span><span class="sxs-lookup"><span data-stu-id="a74af-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="a74af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a74af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74af-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="a74af-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="a74af-108">Especifica um número de identificação universalmente exclusivo para a interface</span><span class="sxs-lookup"><span data-stu-id="a74af-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="a74af-109">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="a74af-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a74af-110">Especifica uma lista de zero ou mais atributos MIDL adicionais.</span><span class="sxs-lookup"><span data-stu-id="a74af-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a74af-111">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="a74af-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a74af-112">O nome da interface à qual o atributo **duplo** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="a74af-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a74af-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a74af-113">Remarks</span></span>

<span data-ttu-id="a74af-114">As interfaces identificadas pelo atributo **Dual** devem ser compatíveis com a automação e ser derivadas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="a74af-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="a74af-115">Este atributo não é permitido em dispinterfaces.</span><span class="sxs-lookup"><span data-stu-id="a74af-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="a74af-116">O atributo **Dual** cria uma interface que é uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e uma interface com (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="a74af-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="a74af-117">As primeiras sete entradas do VTBL para uma interface dupla são os sete membros de **IDispatch**, e as entradas restantes são para o acesso direto aos membros da interface dupla.</span><span class="sxs-lookup"><span data-stu-id="a74af-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="a74af-118">Todos os parâmetros e tipos de retorno especificados para membros de uma interface dupla devem ser tipos compatíveis com a automação.</span><span class="sxs-lookup"><span data-stu-id="a74af-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="a74af-119">Todos os membros de uma interface dupla devem passar um HRESULT como o valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="a74af-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="a74af-120">Membros, como funções de assessor de propriedade, que precisam retornar outros valores, devem especificar o último parâmetro como [**out**](out-idl.md), [**retval**](retval.md), indicando um parâmetro de saída que retorna o valor da função.</span><span class="sxs-lookup"><span data-stu-id="a74af-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="a74af-121">Além disso, os membros que precisam dar suporte a várias localidades devem passar um parâmetro [**LCID**](lcid.md) .</span><span class="sxs-lookup"><span data-stu-id="a74af-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="a74af-122">Uma interface dupla fornece a velocidade da ligação VTBL direta e a flexibilidade da Associação de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a74af-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="a74af-123">Por esse motivo, as interfaces duplas são recomendadas sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="a74af-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="a74af-124">Se seu aplicativo acessa dados de objeto ao converter o *ponteiro dentro* da chamada de interface, você deve verificar os ponteiros de VTBL no objeto em relação aos seus próprios ponteiros do VTBL para garantir que você esteja conectado ao proxy apropriado.</span><span class="sxs-lookup"><span data-stu-id="a74af-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="a74af-125">A especificação de **Dual** em uma interface implica que a interface é compatível com a automação e, portanto, faz com que os \_ sinalizadores TYPEFLAG FDUAL e TYPEFLAG \_ FOLEAUTOMATION sejam definidos.</span><span class="sxs-lookup"><span data-stu-id="a74af-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="a74af-126">Flags</span><span class="sxs-lookup"><span data-stu-id="a74af-126">Flags</span></span>

<span data-ttu-id="a74af-127">TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION</span><span class="sxs-lookup"><span data-stu-id="a74af-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="a74af-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a74af-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="a74af-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a74af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74af-130">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="a74af-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a74af-131">**interface**</span><span class="sxs-lookup"><span data-stu-id="a74af-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="a74af-132">**LCID**</span><span class="sxs-lookup"><span data-stu-id="a74af-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="a74af-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="a74af-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="a74af-134">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="a74af-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a74af-135">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="a74af-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a74af-136">**fora**</span><span class="sxs-lookup"><span data-stu-id="a74af-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a74af-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="a74af-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 