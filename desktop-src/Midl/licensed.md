---
title: atributo licenciado
description: O atributo \ licenciado \ indica que a coclass à qual ele se aplica é licenciado e deve ser instanciada usando IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- atributo licenciado MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007417"
---
# <a name="licensed-attribute"></a><span data-ttu-id="0fa7e-104">atributo licenciado</span><span class="sxs-lookup"><span data-stu-id="0fa7e-104">licensed attribute</span></span>

<span data-ttu-id="0fa7e-105">O atributo **\[ licenciado \]** indica que a [**coclass**](coclass.md) à qual ela se aplica é licenciada e deve ser instanciada usando [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span><span class="sxs-lookup"><span data-stu-id="0fa7e-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="0fa7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fa7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fa7e-107">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="0fa7e-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa7e-108">Especifica zero ou mais atributos que se aplicam à instrução [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa7e-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="0fa7e-109">Os atributos de **coclasse** permitidos são **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ licenciado \]**, **\[** [**version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** e **\[** [**Hidden**](hidden.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0fa7e-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="0fa7e-110">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="0fa7e-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa7e-111">Especifica o nome pelo qual o objeto de componente é conhecido na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0fa7e-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="0fa7e-112">*definição de coclasse*</span><span class="sxs-lookup"><span data-stu-id="0fa7e-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa7e-113">Especifica as instruções que compõem a definição da [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa7e-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fa7e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fa7e-114">Remarks</span></span>

<span data-ttu-id="0fa7e-115">O licenciamento é um recurso do COM que fornece controle sobre a criação de objetos.</span><span class="sxs-lookup"><span data-stu-id="0fa7e-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="0fa7e-116">Os objetos licenciados podem ser criados somente por clientes que estão autorizados a usá-los.</span><span class="sxs-lookup"><span data-stu-id="0fa7e-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="0fa7e-117">O licenciamento é implementado em COM por meio da interface [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) e por suporte para uma chave de licença que pode ser passada em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0fa7e-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="0fa7e-118">Flags</span><span class="sxs-lookup"><span data-stu-id="0fa7e-118">Flags</span></span>

<span data-ttu-id="0fa7e-119">TYPEFLAG \_ FLICENSED</span><span class="sxs-lookup"><span data-stu-id="0fa7e-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="0fa7e-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0fa7e-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="0fa7e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fa7e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fa7e-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="0fa7e-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="0fa7e-123">Conteúdo de uma biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0fa7e-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="0fa7e-124">**controlo**</span><span class="sxs-lookup"><span data-stu-id="0fa7e-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="0fa7e-125">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="0fa7e-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0fa7e-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="0fa7e-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="0fa7e-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="0fa7e-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="0fa7e-128">**oculto**</span><span class="sxs-lookup"><span data-stu-id="0fa7e-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="0fa7e-129">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="0fa7e-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0fa7e-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="0fa7e-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="0fa7e-131">**Versão**</span><span class="sxs-lookup"><span data-stu-id="0fa7e-131">**version**</span></span>](version.md)
</dt> </dl>

 

 