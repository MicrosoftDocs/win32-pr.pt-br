---
title: atributo source
description: O atributo \ Source \ indica que um membro de uma coclass, propriedade ou método é uma fonte de eventos. Para um membro de uma coclass, esse atributo significa que o membro é chamado em vez de implementado.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- atributo de origem MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917179"
---
# <a name="source-attribute"></a><span data-ttu-id="a4a6a-105">atributo source</span><span class="sxs-lookup"><span data-stu-id="a4a6a-105">source attribute</span></span>

<span data-ttu-id="a4a6a-106">O atributo **\[ Source \]** indica que um membro de uma [**coclass**](coclass.md), Property ou Method é uma fonte de eventos.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="a4a6a-107">Para um membro de uma **coclass**, esse atributo significa que o membro é chamado em vez de implementado.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="a4a6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4a6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a6a-109">*coclass-atributos*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-110">Zero ou mais atributos que serão aplicados à [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6a-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-111">*coclass-Name*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-112">O identificador de nome da [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6a-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-113">*opcional-atributos*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-114">Zero ou mais atributos MIDL.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-115">*tipo de instrução*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-116">Pode ser [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6a-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-117">*nome da instrução*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-118">O nome da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6a-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-119">*tipo de objeto*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-120">O tipo do objeto que o método retorna.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-120">The type of the object that the method returns.</span></span> <span data-ttu-id="a4a6a-121">Esse objeto é uma fonte de eventos.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-122">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-123">O nome de um método em uma [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6a-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4a6a-124">*opcional-lista de parâmetros*</span><span class="sxs-lookup"><span data-stu-id="a4a6a-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a6a-125">Zero ou mais parâmetros de método.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4a6a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4a6a-126">Remarks</span></span>

<span data-ttu-id="a4a6a-127">Em uma propriedade ou método, o atributo de **\[ origem \]** indica que o membro retorna um objeto ou uma variante que é uma fonte de eventos.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="a4a6a-128">O objeto implementa **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="a4a6a-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="a4a6a-129">Flags</span><span class="sxs-lookup"><span data-stu-id="a4a6a-129">Flags</span></span>

<span data-ttu-id="a4a6a-130">IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ Source, FUNCFLAG \_ Source</span><span class="sxs-lookup"><span data-stu-id="a4a6a-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="a4a6a-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4a6a-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="a4a6a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4a6a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a6a-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="a4a6a-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="a4a6a-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="a4a6a-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="a4a6a-135">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="a4a6a-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a4a6a-136">**interface**</span><span class="sxs-lookup"><span data-stu-id="a4a6a-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="a4a6a-137">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="a4a6a-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a4a6a-138">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="a4a6a-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a4a6a-139">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="a4a6a-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 