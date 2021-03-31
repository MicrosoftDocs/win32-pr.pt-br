---
title: strict_context_handle atributo
description: O atributo \ estrito \_ identificador de contexto \_ \ ACF define restrições em identificadores de contexto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle do atributo MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917178"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="6c89c-104">atributo de identificador de \_ contexto estrito \_</span><span class="sxs-lookup"><span data-stu-id="6c89c-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="6c89c-105">O atributo ACF do **\[ \_ \_ identificador \] de contexto estrito** define restrições em identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="6c89c-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="6c89c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c89c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c89c-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="6c89c-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6c89c-108">Outros atributos de ACF que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="6c89c-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="6c89c-109">Os atributos válidos [**incluem \_ identificador automático**](auto-handle.md), [**\_ identificador implícito**](implicit-handle.md), [**\_ identificador explícito**](explicit-handle.md)e [**otimizar**](optimize.md), [**código**](code.md)ou [**Nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="6c89c-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="6c89c-110">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6c89c-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6c89c-111">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="6c89c-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6c89c-112">O nome da interface.</span><span class="sxs-lookup"><span data-stu-id="6c89c-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="6c89c-113">*instruções de definição de interface*</span><span class="sxs-lookup"><span data-stu-id="6c89c-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="6c89c-114">Uma ou mais instruções MIDL que definem os elementos da [**interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="6c89c-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c89c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c89c-115">Remarks</span></span>

<span data-ttu-id="6c89c-116">Normalmente, quando uma chamada para um método de interface gera um identificador de contexto, esse identificador se torna livremente disponível para qualquer outra interface.</span><span class="sxs-lookup"><span data-stu-id="6c89c-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="6c89c-117">Ao usar o atributo de **\[ \_ \_ identificador \] de contexto estrito** , você garante que os métodos nessa interface só aceitarão identificadores de contexto que foram criados por um método da mesma interface.</span><span class="sxs-lookup"><span data-stu-id="6c89c-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="6c89c-118">Interfaces compiladas sem **\[ \_ \_ identificador \] de contexto estrito** não podem aceitar identificadores de contexto criados em interfaces compiladas com **\[ \_ \_ \] identificador de contexto estrito**.</span><span class="sxs-lookup"><span data-stu-id="6c89c-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c89c-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6c89c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c89c-120">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="6c89c-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="6c89c-121">**auto-completar**</span><span class="sxs-lookup"><span data-stu-id="6c89c-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="6c89c-122">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="6c89c-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="6c89c-123">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="6c89c-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="6c89c-124">**identificador de contexto \_ \_ noserializeize**</span><span class="sxs-lookup"><span data-stu-id="6c89c-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="6c89c-125">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="6c89c-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="6c89c-126">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="6c89c-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="6c89c-127">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="6c89c-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="6c89c-128">**formato**</span><span class="sxs-lookup"><span data-stu-id="6c89c-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="6c89c-129">tipo \_ de \_ identificador de contexto estrito \_</span><span class="sxs-lookup"><span data-stu-id="6c89c-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 