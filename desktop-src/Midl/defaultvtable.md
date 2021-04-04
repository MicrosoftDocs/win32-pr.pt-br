---
title: atributo defaultvtable
description: O atributo \ defaultvtable \ define uma interface como a interface padrão vtable.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- MIDL de atributo defaultvtable
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823737"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="c52e0-104">atributo defaultvtable</span><span class="sxs-lookup"><span data-stu-id="c52e0-104">defaultvtable attribute</span></span>

<span data-ttu-id="c52e0-105">O atributo **\[ defaultvtable \]** define uma interface como a interface padrão vtable.</span><span class="sxs-lookup"><span data-stu-id="c52e0-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="c52e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c52e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c52e0-107">*Categoria-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="c52e0-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c52e0-108">Outros atributos que se aplicam à classe.</span><span class="sxs-lookup"><span data-stu-id="c52e0-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="c52e0-109">Os **\[** atributos de [**origem**](source.md) **\]** e **\[** [**UUID**](uuid.md) **\]** são necessários.</span><span class="sxs-lookup"><span data-stu-id="c52e0-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="c52e0-110">*coclass-Name*</span><span class="sxs-lookup"><span data-stu-id="c52e0-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c52e0-111">O nome da classe.</span><span class="sxs-lookup"><span data-stu-id="c52e0-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c52e0-112">*lista de interface de coclasse*</span><span class="sxs-lookup"><span data-stu-id="c52e0-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c52e0-113">Uma lista de interfaces para a classe.</span><span class="sxs-lookup"><span data-stu-id="c52e0-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c52e0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c52e0-114">Remarks</span></span>

<span data-ttu-id="c52e0-115">Uma interface vtable padrão não pode ser um dispinterface — ela deve ser uma interface dupla ou vtable.</span><span class="sxs-lookup"><span data-stu-id="c52e0-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="c52e0-116">Se a interface for uma interface dupla, os coletores poderão assumir que receberão eventos por meio de vtable.</span><span class="sxs-lookup"><span data-stu-id="c52e0-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="c52e0-117">Uma classe pode ser uma interface de origem padrão e uma interface de origem vtable padrão, conforme mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="c52e0-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="c52e0-118">Nesse caso, um coletor de aviso deve usar IID \_ IDISPATCH para receber eventos de expedição e usar o identificador de interface para receber eventos vtable.</span><span class="sxs-lookup"><span data-stu-id="c52e0-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="c52e0-119">Representação TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="c52e0-119">Typeflag Representation</span></span>

<span data-ttu-id="c52e0-120">A presença de IMPLTYPEFLAG \_ FDEFAULTVTABLE.</span><span class="sxs-lookup"><span data-stu-id="c52e0-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="c52e0-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c52e0-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c52e0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c52e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52e0-123">**coclass**</span><span class="sxs-lookup"><span data-stu-id="c52e0-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="c52e0-124">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="c52e0-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c52e0-125">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="c52e0-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c52e0-126">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="c52e0-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c52e0-127">**original**</span><span class="sxs-lookup"><span data-stu-id="c52e0-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="c52e0-128">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="c52e0-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 