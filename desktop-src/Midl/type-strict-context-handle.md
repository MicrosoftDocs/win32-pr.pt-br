---
title: type_strict_context_handle atributo
description: Use o identificador de \_ contexto estrito \ Type \_ \_ \ em um arquivo ACF para definir restrições em identificadores de contexto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle do atributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453983"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="d1a5c-104">tipo \_ de \_ atributo de identificador de contexto estrito \_</span><span class="sxs-lookup"><span data-stu-id="d1a5c-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="d1a5c-105">Use o **\[ \_ \_ \_ identificador \] de contexto estrito de tipo** em um arquivo ACF para definir restrições em identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="d1a5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1a5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a5c-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="d1a5c-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5c-108">Outros atributos de ACF que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="d1a5c-109">Os atributos válidos [**incluem \_ identificador automático**](auto-handle.md), [**\_ identificador implícito**](implicit-handle.md), [**\_ identificador explícito**](explicit-handle.md)e [**otimizar**](optimize.md), [**código**](code.md)ou [**Nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="d1a5c-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="d1a5c-110">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5c-111">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="d1a5c-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5c-112">O nome da interface.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5c-113">*instruções de definição de interface*</span><span class="sxs-lookup"><span data-stu-id="d1a5c-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5c-114">Uma ou mais instruções MIDL que definem os elementos da [**interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="d1a5c-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1a5c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1a5c-115">Remarks</span></span>

<span data-ttu-id="d1a5c-116">Para usar esse atributo, o sinalizador-Target deve ser definido como NT60 (ou superior) durante a execução de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="d1a5c-117">\[tipo \_ \_ \_ de identificador de contexto estrito \] é um superconjunto funcional de \[ identificador de \_ contexto estrito \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d1a5c-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="d1a5c-118">No \[ \_ \_ identificador de contexto estrito \] , a ID de tipo do identificador é sempre 0; no \[ identificador de contexto de tipo \_ estrito \_ \_ \] , uma ID de tipo exclusivo é atribuída pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="d1a5c-119">É recomendável usar o \[ \_ \_ \_ identificador de contexto de tipo estrito \] em vez do \[ identificador de \_ contexto estrito \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d1a5c-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="d1a5c-120">Os identificadores de contexto não são associados a um tipo específico por padrão.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="d1a5c-121">Quando vários tipos de identificadores de contexto são usados no mesmo processo, é possível que um cliente mal-intencionado passe um identificador de contexto em vez de outro para produzir resultados indesejáveis.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="d1a5c-122">O uso do \[ identificador de contexto de tipo \_ estrito \_ \_ \] permite que os aplicativos imponham a consistência de tipo de identificador de contexto e evitem qualquer uso de tipo de identificador de contexto incompatível.</span><span class="sxs-lookup"><span data-stu-id="d1a5c-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="d1a5c-123">Um identificador de contexto atribuído com o \[ identificador de contexto de tipo \_ estrito \_ \_ \] também não pode ser atribuído com um \[ identificador de \_ contexto estrito \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d1a5c-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="d1a5c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1a5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a5c-125">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="d1a5c-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-126">**auto-completar**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-127">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="d1a5c-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="d1a5c-128">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-129">**identificador de contexto \_ \_ noserializeize**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-130">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-131">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-132">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-133">**formato**</span><span class="sxs-lookup"><span data-stu-id="d1a5c-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="d1a5c-134">\_identificador de contexto estrito \_</span><span class="sxs-lookup"><span data-stu-id="d1a5c-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 