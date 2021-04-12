---
title: atributo uidefault
description: O atributo \ uidefault \ indica que o membro de informações de tipo é o membro padrão para exibição na interface do usuário.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault do atributo MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365868"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="ddbd9-104">atributo uidefault</span><span class="sxs-lookup"><span data-stu-id="ddbd9-104">uidefault attribute</span></span>

<span data-ttu-id="ddbd9-105">O atributo **\[ uidefault \]** indica que o membro de informações de tipo é o membro padrão para exibição na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="ddbd9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddbd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddbd9-107">*lista de atributos de método*</span><span class="sxs-lookup"><span data-stu-id="ddbd9-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbd9-108">Outros atributos que se aplicam ao método.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="ddbd9-109">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="ddbd9-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbd9-110">O tipo dos dados que o método retornará quando concluir a execução.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="ddbd9-111">*nome do método*</span><span class="sxs-lookup"><span data-stu-id="ddbd9-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbd9-112">O nome do método.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="ddbd9-113">*lista de parâmetros de método*</span><span class="sxs-lookup"><span data-stu-id="ddbd9-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbd9-114">Zero ou mais parâmetros para o método.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddbd9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddbd9-115">Remarks</span></span>

<span data-ttu-id="ddbd9-116">Aplicar o atributo **\[ uidefault \]** a um membro de uma interface ou uma dispinterface informa Visual Basic, em tempo de design, para exibir automaticamente esse evento ou propriedade para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="ddbd9-117">Isso significa que quando o usuário clica duas vezes em um objeto, Visual Basic salta para o evento na interface de origem padrão que tem o atributo **\[ uidefault \]** .</span><span class="sxs-lookup"><span data-stu-id="ddbd9-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="ddbd9-118">Quando o usuário seleciona um objeto, Visual Basic navegador de Propriedades exibe a propriedade na interface de origem padrão que tem esse atributo.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="ddbd9-119">Se nenhum evento ou propriedade tiver o atributo **\[ uidefault \]** , Visual Basic exibirá o primeiro evento ou Propriedade listado na interface padrão.</span><span class="sxs-lookup"><span data-stu-id="ddbd9-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="ddbd9-120">Representação TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="ddbd9-120">Typeflag Representation</span></span>

<span data-ttu-id="ddbd9-121">A presença de FUNCFLAG \_ FUIDEFAULT ou VARFLAG \_ FUIDEFAULT</span><span class="sxs-lookup"><span data-stu-id="ddbd9-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="ddbd9-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ddbd9-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="ddbd9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddbd9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbd9-124">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="ddbd9-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ddbd9-125">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="ddbd9-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ddbd9-126">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="ddbd9-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 