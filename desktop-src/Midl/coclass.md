---
title: atributo coclass
description: A instrução coclass fornece uma lista das interfaces com suporte para um objeto de componente.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- atributo de coclasse MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365949"
---
# <a name="coclass-attribute"></a><span data-ttu-id="f321d-104">atributo coclass</span><span class="sxs-lookup"><span data-stu-id="f321d-104">coclass attribute</span></span>

<span data-ttu-id="f321d-105">A instrução **coclass** fornece uma lista das interfaces com suporte para um objeto de componente.</span><span class="sxs-lookup"><span data-stu-id="f321d-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="f321d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f321d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f321d-107">*Categoria-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="f321d-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f321d-108">O **\[** atributo [**UUID**](uuid.md) **\]** é necessário em uma **coclass**.</span><span class="sxs-lookup"><span data-stu-id="f321d-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="f321d-109">Esse é o mesmo **\[ UUID \]** registrado como um CLSID no banco de dados de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="f321d-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="f321d-110">Os **\[** atributos [**HelpString**](helpstring.md) **\]** , **\[** [**IdentificaçãoDoContextoDaAjuda**](helpcontext.md) **\]** , **\[** [**licenciado**](licensed.md) **\]** , **\[** [**versão**](version.md) **\]** , **\[** [**controle**](control.md) **\]** , **\[** [**oculto**](hidden.md) **\]** e **\[** [**appobject**](appobject.md) **\]** são aceitos, mas não obrigatórios, antes de uma definição de **coclasse** .</span><span class="sxs-lookup"><span data-stu-id="f321d-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="f321d-111">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="f321d-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="f321d-112">Nome pelo qual o objeto comum é conhecido na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="f321d-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="f321d-113">*atributos de interface*</span><span class="sxs-lookup"><span data-stu-id="f321d-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f321d-114">Atributos opcionais para a interface ou Dispinterface.</span><span class="sxs-lookup"><span data-stu-id="f321d-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="f321d-115">Os **\[** atributos de [**origem**](source.md) **\]** , **\[** [**padrão**](default.md) **\]** e **\[** [**restritos**](restricted.md) **\]** são aceitos em uma interface ou dispinterface dentro de uma **coclass**.</span><span class="sxs-lookup"><span data-stu-id="f321d-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="f321d-116">*InterfaceName*</span><span class="sxs-lookup"><span data-stu-id="f321d-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="f321d-117">Uma interface declarada com a palavra-chave [**interface**](interface.md) ou uma dispinterface declarada com a palavra-chave [**dispinterface**](dispinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="f321d-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f321d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f321d-118">Remarks</span></span>

<span data-ttu-id="f321d-119">O Microsoft Component Object Model define uma classe como uma implementação que permite **QueryInterface** entre um conjunto de interfaces.</span><span class="sxs-lookup"><span data-stu-id="f321d-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="f321d-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f321d-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="f321d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f321d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f321d-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="f321d-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="f321d-123">**controlo**</span><span class="sxs-lookup"><span data-stu-id="f321d-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="f321d-124">**os**</span><span class="sxs-lookup"><span data-stu-id="f321d-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="f321d-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="f321d-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="f321d-126">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="f321d-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f321d-127">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="f321d-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f321d-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="f321d-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="f321d-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="f321d-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="f321d-130">**oculto**</span><span class="sxs-lookup"><span data-stu-id="f321d-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="f321d-131">**interface**</span><span class="sxs-lookup"><span data-stu-id="f321d-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="f321d-132">**licensed**</span><span class="sxs-lookup"><span data-stu-id="f321d-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="f321d-133">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="f321d-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f321d-134">**Restricted**</span><span class="sxs-lookup"><span data-stu-id="f321d-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="f321d-135">**original**</span><span class="sxs-lookup"><span data-stu-id="f321d-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="f321d-136">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="f321d-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="f321d-137">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="f321d-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="f321d-138">**Versão**</span><span class="sxs-lookup"><span data-stu-id="f321d-138">**version**</span></span>](version.md)
</dt> </dl>

 

 