---
title: atributo defaultcollelem
description: O atributo \ defaultcollelem \ sinaliza uma propriedade como uma função de acessador para um elemento da coleção padrão.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- defaultcollelem do atributo MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007494"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="7f36e-104">atributo defaultcollelem</span><span class="sxs-lookup"><span data-stu-id="7f36e-104">defaultcollelem attribute</span></span>

<span data-ttu-id="7f36e-105">O atributo **\[ defaultcollelem \]** sinaliza uma propriedade como uma função de acessador para um elemento da coleção padrão.</span><span class="sxs-lookup"><span data-stu-id="7f36e-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="7f36e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f36e-107">*Propriedade-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="7f36e-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7f36e-108">Outros atributos que se aplicam à propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f36e-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="7f36e-109">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="7f36e-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7f36e-110">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="7f36e-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7f36e-111">*nome da propriedade*</span><span class="sxs-lookup"><span data-stu-id="7f36e-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7f36e-112">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f36e-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="7f36e-113">*prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="7f36e-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7f36e-114">Uma lista de zero ou mais parâmetros associados à propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f36e-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f36e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f36e-115">Remarks</span></span>

<span data-ttu-id="7f36e-116">O atributo **\[ defaultcollelem \]** é usado para a otimização de código do Visual BasicÂ®.</span><span class="sxs-lookup"><span data-stu-id="7f36e-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="7f36e-117">Se um membro de uma interface ou dispinterface for sinalizado como uma função de acessador, a chamada vai diretamente para esse membro.</span><span class="sxs-lookup"><span data-stu-id="7f36e-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="7f36e-118">O uso de **\[ defaultcollelem \]** deve ser consistente para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f36e-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="7f36e-119">Por exemplo, se você usar o atributo em uma propriedade *Get* , ele também deverá estar presente em uma propriedade *Let* .</span><span class="sxs-lookup"><span data-stu-id="7f36e-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="7f36e-120">Representação TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7f36e-120">Typeflags Representation</span></span>

<span data-ttu-id="7f36e-121">A presença de FUNCFLAG \_ FDEFAULTCOLLELEM ou VARFLAG \_ FDEFAULTCOLLELEM.</span><span class="sxs-lookup"><span data-stu-id="7f36e-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="7f36e-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f36e-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="7f36e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f36e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f36e-124">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="7f36e-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7f36e-125">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="7f36e-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7f36e-126">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="7f36e-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 