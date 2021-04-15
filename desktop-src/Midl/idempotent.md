---
title: atributo idempotente
description: O atributo \ idempotente \ especifica que uma operação não modifica informações de estado e retorna os mesmos resultados toda vez que é executada. Executar a rotina mais de uma vez tem o mesmo efeito que executá-la uma vez.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- MIDL de atributo idempotente
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498854"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="d7b28-105">atributo idempotente</span><span class="sxs-lookup"><span data-stu-id="d7b28-105">idempotent attribute</span></span>

<span data-ttu-id="d7b28-106">O atributo **\[ idempotente \]** especifica que uma operação não modifica informações de estado e retorna os mesmos resultados toda vez que é executada.</span><span class="sxs-lookup"><span data-stu-id="d7b28-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="d7b28-107">Executar a rotina mais de uma vez tem o mesmo efeito que executá-la uma vez.</span><span class="sxs-lookup"><span data-stu-id="d7b28-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="d7b28-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7b28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b28-109">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="d7b28-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b28-110">Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="d7b28-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="d7b28-111">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="d7b28-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="d7b28-112">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="d7b28-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b28-113">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="d7b28-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d7b28-114">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="d7b28-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b28-115">Especifica atributos adicionais a serem aplicados à função.</span><span class="sxs-lookup"><span data-stu-id="d7b28-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="d7b28-116">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="d7b28-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d7b28-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="d7b28-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b28-118">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="d7b28-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="d7b28-119">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="d7b28-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b28-120">Especifica o nome da função à qual o atributo **\[ idempotente \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="d7b28-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="d7b28-121">*params*</span><span class="sxs-lookup"><span data-stu-id="d7b28-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b28-122">Lista de parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="d7b28-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7b28-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7b28-123">Remarks</span></span>

<span data-ttu-id="d7b28-124">O RPC dá suporte a dois tipos de semântica de chamada remota: chamadas para operações com o atributo **\[ idempotente \]** e chamadas para operações (operações *idempotentes* ) sem o atributo **\[ idempotente \]** (operações *não idempotentes* ).</span><span class="sxs-lookup"><span data-stu-id="d7b28-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="d7b28-125">Uma operação idempotente pode ser executada mais de uma vez sem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="d7b28-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="d7b28-126">Por outro lado, uma operação não idempotente não pode ser executada mais de uma vez, pois ela retornará resultados diferentes a cada vez ou, por isso, modificará algum estado.</span><span class="sxs-lookup"><span data-stu-id="d7b28-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="d7b28-127">Para garantir que um procedimento seja automaticamente executado novamente se a chamada não for concluída, use o atributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="d7b28-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="d7b28-128">Se os atributos **\[ idempotente \]**, **\[** [**Broadcast**](broadcast.md) **\]** ou **\[** [**talvez**](maybe.md) **\]** não estiverem presentes, o procedimento usará semânticas não idempotentes por padrão.</span><span class="sxs-lookup"><span data-stu-id="d7b28-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="d7b28-129">Nesse caso, a operação é executada apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="d7b28-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7b28-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b28-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b28-131">**difusor**</span><span class="sxs-lookup"><span data-stu-id="d7b28-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="d7b28-132">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="d7b28-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d7b28-133">**Eu**</span><span class="sxs-lookup"><span data-stu-id="d7b28-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




