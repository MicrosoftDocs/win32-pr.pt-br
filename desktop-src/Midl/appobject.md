---
title: atributo appobject
description: O atributo \ appobject \ identifica a coclass como um objeto de aplicativo, que está associado a um aplicativo EXE completo.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject do atributo MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365898"
---
# <a name="appobject-attribute"></a><span data-ttu-id="54cdb-104">atributo appobject</span><span class="sxs-lookup"><span data-stu-id="54cdb-104">appobject attribute</span></span>

<span data-ttu-id="54cdb-105">O atributo **\[ appobject \]** identifica a [**coclass**](coclass.md) como um objeto Application, que está associado a um aplicativo exe completo.</span><span class="sxs-lookup"><span data-stu-id="54cdb-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="54cdb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54cdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54cdb-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="54cdb-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="54cdb-108">Especifica um número de identificação universalmente exclusivo para a [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="54cdb-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="54cdb-109">*Categoria-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="54cdb-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="54cdb-110">Especifica zero ou mais atributos que se aplicam à instrução [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="54cdb-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="54cdb-111">Os atributos **de coclasse** permitidos são [**\[ \] HelpString**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ licenciado \]**](licensed.md), [**\[ version \]**](version.md), [**\[ Control \]**](control.md)e [**\[ Hidden \]**](hidden.md).</span><span class="sxs-lookup"><span data-stu-id="54cdb-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="54cdb-112">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="54cdb-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="54cdb-113">Especifica o nome pelo qual o objeto de componente é conhecido na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="54cdb-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="54cdb-114">*definição de coclasse*</span><span class="sxs-lookup"><span data-stu-id="54cdb-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="54cdb-115">Especifica as instruções que compõem a definição da [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="54cdb-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54cdb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="54cdb-116">Remarks</span></span>

<span data-ttu-id="54cdb-117">O atributo **\[ appobject \]** também indica que as funções e as propriedades da [**coclass**](coclass.md) estão disponíveis globalmente na biblioteca de tipos atual.</span><span class="sxs-lookup"><span data-stu-id="54cdb-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="54cdb-118">A representação TYPEFLAG para esse atributo é TYPEFLAG \_ FAPPOBJECT</span><span class="sxs-lookup"><span data-stu-id="54cdb-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="54cdb-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54cdb-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="54cdb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="54cdb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cdb-121">**coclass**</span><span class="sxs-lookup"><span data-stu-id="54cdb-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="54cdb-122">**controlo**</span><span class="sxs-lookup"><span data-stu-id="54cdb-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="54cdb-123">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="54cdb-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="54cdb-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="54cdb-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="54cdb-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="54cdb-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="54cdb-126">**oculto**</span><span class="sxs-lookup"><span data-stu-id="54cdb-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="54cdb-127">**licensed**</span><span class="sxs-lookup"><span data-stu-id="54cdb-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="54cdb-128">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="54cdb-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="54cdb-129">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="54cdb-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="54cdb-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="54cdb-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="54cdb-131">**Versão**</span><span class="sxs-lookup"><span data-stu-id="54cdb-131">**version**</span></span>](version.md)
</dt> </dl>

 

 