---
title: atributo agregável
description: O atributo \ agregável \ indica que a classe oferece suporte à agregação.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- MIDL de atributo agregável
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293962"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="c514e-104">atributo agregável</span><span class="sxs-lookup"><span data-stu-id="c514e-104">aggregatable attribute</span></span>

<span data-ttu-id="c514e-105">O atributo **\[ agregável \]** indica que a classe oferece suporte à agregação.</span><span class="sxs-lookup"><span data-stu-id="c514e-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="c514e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c514e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c514e-107">*Categoria-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="c514e-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c514e-108">Outros atributos que se aplicam à classe.</span><span class="sxs-lookup"><span data-stu-id="c514e-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="c514e-109">*coclass-Name*</span><span class="sxs-lookup"><span data-stu-id="c514e-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c514e-110">O nome da classe.</span><span class="sxs-lookup"><span data-stu-id="c514e-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c514e-111">*lista de interface de coclasse*</span><span class="sxs-lookup"><span data-stu-id="c514e-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c514e-112">Uma lista de interfaces para a classe.</span><span class="sxs-lookup"><span data-stu-id="c514e-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c514e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c514e-113">Remarks</span></span>

<span data-ttu-id="c514e-114">Use o atributo **\[ agregável \]** em uma instrução [**coclass**](coclass.md) para permitir que os usuários saibam que a classe oferece suporte a agregações.</span><span class="sxs-lookup"><span data-stu-id="c514e-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="c514e-115">Ou seja, a classe permite que suas interfaces sejam expostas por uma classe de contêiner como se essas interfaces fossem as próprias interfaces do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c514e-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="c514e-116">A representação TYPEFLAG para esse atributo é TYPEFLAG \_ FAGGREGATABLE.</span><span class="sxs-lookup"><span data-stu-id="c514e-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="c514e-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c514e-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="c514e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c514e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c514e-119">**coclass**</span><span class="sxs-lookup"><span data-stu-id="c514e-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="c514e-120">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="c514e-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c514e-121">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="c514e-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c514e-122">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="c514e-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 