---
title: atributo noncreatable
description: O atributo \ não define um objeto que não pode ser instanciado por si só.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL de atributo não-cri
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293951"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="d41df-104">atributo noncreatable</span><span class="sxs-lookup"><span data-stu-id="d41df-104">noncreatable attribute</span></span>

<span data-ttu-id="d41df-105">O atributo não- **\[ cri \]** define um objeto que não pode ser instanciado por si só.</span><span class="sxs-lookup"><span data-stu-id="d41df-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="d41df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d41df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41df-107">*Categoria-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="d41df-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d41df-108">Outros atributos que se aplicam à classe.</span><span class="sxs-lookup"><span data-stu-id="d41df-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="d41df-109">*coclass-Name*</span><span class="sxs-lookup"><span data-stu-id="d41df-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d41df-110">O nome da classe.</span><span class="sxs-lookup"><span data-stu-id="d41df-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="d41df-111">*lista de interface de coclasse*</span><span class="sxs-lookup"><span data-stu-id="d41df-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d41df-112">Uma lista de interfaces para a classe.</span><span class="sxs-lookup"><span data-stu-id="d41df-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d41df-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d41df-113">Remarks</span></span>

<span data-ttu-id="d41df-114">Use o **\[ \] atributo não** criável em uma instrução [**coclass**](coclass.md) para indicar aos usuários que eles não podem criar um novo objeto dessa classe no nível superior — ou seja, chamando **CreateInstance** ou **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d41df-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="d41df-115">A instanciação de um objeto dessa classe requer uma chamada de método para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="d41df-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="d41df-116">Por exemplo, no Microsoft Excel, o objeto "Cell" não pode ser acessado e deve ser obtido de um objeto planilha do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d41df-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="d41df-117">Os métodos que retornam instâncias de classes não-retornáveis devem retornar o tipo exato do objeto, em vez de tipos **Variant** ou **IDispatch** \* .</span><span class="sxs-lookup"><span data-stu-id="d41df-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="d41df-118">Representação de TYPEFLAG:</span><span class="sxs-lookup"><span data-stu-id="d41df-118">Typeflag Representation:</span></span>

<span data-ttu-id="d41df-119">A ausência de TYPEFLAG \_ FCANCREATE.</span><span class="sxs-lookup"><span data-stu-id="d41df-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="d41df-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d41df-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="d41df-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d41df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41df-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="d41df-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="d41df-123">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d41df-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d41df-124">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d41df-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d41df-125">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="d41df-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 