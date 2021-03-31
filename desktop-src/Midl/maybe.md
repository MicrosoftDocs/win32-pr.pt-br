---
title: atributo talvez
description: A palavra-chave \ talvez \ indica que a chamada de procedimento remoto não precisa ser executada toda vez que é chamada e o cliente não espera uma resposta. Observe que o protocolo \ talvez \ não garante nenhuma entrega nem conclusão da chamada.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- Talvez o atributo MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006374"
---
# <a name="maybe-attribute"></a><span data-ttu-id="c6c8f-105">atributo talvez</span><span class="sxs-lookup"><span data-stu-id="c6c8f-105">maybe attribute</span></span>

<span data-ttu-id="c6c8f-106">A palavra-chave **\[ pode \]** indicar que a chamada de procedimento remoto não precisa ser executada toda vez que é chamada e o cliente não espera uma resposta.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="c6c8f-107">Observe que o protocolo **\[ talvez \]** não garante nenhuma entrega nem conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="c6c8f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6c8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c8f-109">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="c6c8f-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c8f-110">Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="c6c8f-111">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="c6c8f-112">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="c6c8f-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c8f-113">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="c6c8f-114">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="c6c8f-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c8f-115">Especifica atributos adicionais a serem aplicados à função.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="c6c8f-116">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c6c8f-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="c6c8f-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c8f-118">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="c6c8f-119">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="c6c8f-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c8f-120">Especifica o nome da função à qual o atributo **\[ talvez \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="c6c8f-121">*params*</span><span class="sxs-lookup"><span data-stu-id="c6c8f-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c8f-122">Lista de parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="c6c8f-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6c8f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6c8f-123">Remarks</span></span>

<span data-ttu-id="c6c8f-124">Uma chamada com o atributo de **\[ talvez \]** não pode conter parâmetros de saída e é implicitamente uma **\[** chamada [**idempotente**](idempotent.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="c6c8f-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6c8f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6c8f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c8f-126">**difusor**</span><span class="sxs-lookup"><span data-stu-id="c6c8f-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="c6c8f-127">**idempotente**</span><span class="sxs-lookup"><span data-stu-id="c6c8f-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="c6c8f-128">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="c6c8f-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




