---
title: auto_handle atributo
description: O atributo \ \_ identificador auto \ ACF direciona o stub para estabelecer automaticamente a associação para uma função que não tem um parâmetro de identificador de ligação explícito. Observe que esse atributo está obsoleto e não tem mais suporte.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle do atributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453763"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="1a20b-104">\_manipular atributo automaticamente</span><span class="sxs-lookup"><span data-stu-id="1a20b-104">auto\_handle attribute</span></span>

<span data-ttu-id="1a20b-105">O atributo de ACF de **\[ \_ identificador \] automático** direciona o stub para estabelecer automaticamente a associação para uma função que não tem um parâmetro de identificador de ligação explícito.</span><span class="sxs-lookup"><span data-stu-id="1a20b-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="1a20b-106">Este atributo está obsoleto e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="1a20b-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="1a20b-107">O uso da opção [**/robust**](-robust.md) é recomendado.</span><span class="sxs-lookup"><span data-stu-id="1a20b-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="1a20b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a20b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a20b-109">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="1a20b-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a20b-110">Especifica zero ou mais atributos que se aplicam à interface como um todo, como [**código**](code.md) ou [**Nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="1a20b-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="1a20b-111">Separe os atributos de interface com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="1a20b-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="1a20b-112">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="1a20b-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1a20b-113">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="1a20b-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1a20b-114">*interface-definição*</span><span class="sxs-lookup"><span data-stu-id="1a20b-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="1a20b-115">Especifica as instruções IDL que formam a definição da interface.</span><span class="sxs-lookup"><span data-stu-id="1a20b-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a20b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a20b-116">Remarks</span></span>

<span data-ttu-id="1a20b-117">O atributo **\[ \_ identificador \] automático** é exibido no cabeçalho da interface do ACF.</span><span class="sxs-lookup"><span data-stu-id="1a20b-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="1a20b-118">Ele também aparece no cabeçalho da interface do arquivo IDL quando você especifica a [**\_ configuração do/App**](-app-config.md)do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="1a20b-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="1a20b-119">Quando o cliente chama uma função que usa associação automática e nenhuma associação a um servidor existe, o stub estabelece automaticamente a associação.</span><span class="sxs-lookup"><span data-stu-id="1a20b-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="1a20b-120">A associação é reutilizada para chamadas subsequentes para outras funções na interface que usam associação automática.</span><span class="sxs-lookup"><span data-stu-id="1a20b-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="1a20b-121">O programa de aplicativo cliente não precisa declarar ou executar nenhum processamento relacionado ao identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="1a20b-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="1a20b-122">Quando o ACF não estiver presente ou não incluir o atributo de [**\[ \_ identificador \] implícito**](implicit-handle.md) , o compilador MIDL usará o **\[ \_ \] identificador auto** e emitirá uma mensagem informativa.</span><span class="sxs-lookup"><span data-stu-id="1a20b-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="1a20b-123">O compilador MIDL também usa o **\[ \_ identificador \] auto**, se necessário, para estabelecer a associação inicial para um [**\[ \_ identificador \] de contexto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="1a20b-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="1a20b-124">O atributo de **\[ \_ identificador \] automático** só poderá ocorrer se o [**\[ \_ identificador \] implícito**](implicit-handle.md) ou o atributo de [**\[ \_ identificador \] explícito**](explicit-handle.md) não ocorrer.</span><span class="sxs-lookup"><span data-stu-id="1a20b-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="1a20b-125">O atributo de **\[ \_ identificador \] automático** pode ocorrer no cabeçalho de interface ACF ou IDL no máximo uma vez.</span><span class="sxs-lookup"><span data-stu-id="1a20b-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="1a20b-126">Você não poderá usar a associação automática (com o atributo **\[ \_ identificador \] automático** ou por padrão) se estiver processando dados por meio de pipes.</span><span class="sxs-lookup"><span data-stu-id="1a20b-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1a20b-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a20b-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="1a20b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a20b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a20b-129">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="1a20b-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="1a20b-130">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="1a20b-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="1a20b-131">**auto-completar**</span><span class="sxs-lookup"><span data-stu-id="1a20b-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="1a20b-132">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="1a20b-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="1a20b-133">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="1a20b-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="1a20b-134">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="1a20b-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="1a20b-135">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="1a20b-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




