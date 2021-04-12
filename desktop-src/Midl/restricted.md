---
title: atributo restrito
description: O atributo \ Restricted \ especifica que uma biblioteca ou membro de um módulo, interface ou Dispinterface não pode ser chamado arbitrariamente.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- atributo restrito MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365947"
---
# <a name="restricted-attribute"></a><span data-ttu-id="658a7-104">atributo restrito</span><span class="sxs-lookup"><span data-stu-id="658a7-104">restricted attribute</span></span>

<span data-ttu-id="658a7-105">O atributo **\[ Restricted \]** especifica que uma biblioteca ou membro de um módulo, interface ou Dispinterface não pode ser chamado arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="658a7-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="658a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="658a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="658a7-107">*outros atributos*</span><span class="sxs-lookup"><span data-stu-id="658a7-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="658a7-108">Zero ou mais atributos MIDL.</span><span class="sxs-lookup"><span data-stu-id="658a7-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="658a7-109">*tipo de instrução*</span><span class="sxs-lookup"><span data-stu-id="658a7-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="658a7-110">Um dos seguintes: [**biblioteca**](library.md), [**módulo**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="658a7-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="658a7-111">*nome da instrução*</span><span class="sxs-lookup"><span data-stu-id="658a7-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="658a7-112">O identificador pelo qual o software se refere a essa instrução.</span><span class="sxs-lookup"><span data-stu-id="658a7-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="658a7-113">*definições*</span><span class="sxs-lookup"><span data-stu-id="658a7-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="658a7-114">Elementos de linguagem MIDL que definem o conteúdo desta instrução.</span><span class="sxs-lookup"><span data-stu-id="658a7-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="658a7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="658a7-115">Remarks</span></span>

<span data-ttu-id="658a7-116">Esse atributo permite que você controle o acesso a elementos de interfaces, bibliotecas, módulos e dispinterfaces.</span><span class="sxs-lookup"><span data-stu-id="658a7-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="658a7-117">Por exemplo, ele pode impedir que um item de dados seja usado por um programador de macro.</span><span class="sxs-lookup"><span data-stu-id="658a7-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="658a7-118">Você pode aplicar esse atributo a um membro de uma [**coclass**](coclass.md), independentemente de o membro ser uma dispinterface ou interface, e independentemente de o membro ser um coletor (entrada) ou origem (saída).</span><span class="sxs-lookup"><span data-stu-id="658a7-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="658a7-119">Um membro de uma **coclass** não pode ter os atributos **\[ Default \]** e **\[ Restricted \]** .</span><span class="sxs-lookup"><span data-stu-id="658a7-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="658a7-120">Flags</span><span class="sxs-lookup"><span data-stu-id="658a7-120">Flags</span></span>

<span data-ttu-id="658a7-121">IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="658a7-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="658a7-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="658a7-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="658a7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="658a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658a7-124">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="658a7-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="658a7-125">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="658a7-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="658a7-126">**interface**</span><span class="sxs-lookup"><span data-stu-id="658a7-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="658a7-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="658a7-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="658a7-128">**modulo**</span><span class="sxs-lookup"><span data-stu-id="658a7-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="658a7-129">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="658a7-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="658a7-130">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="658a7-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="658a7-131">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="658a7-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 