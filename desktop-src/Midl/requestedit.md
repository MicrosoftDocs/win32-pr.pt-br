---
title: atributo requestedit
description: O atributo \ requestedit \ indica que a propriedade dá suporte à notificação OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit do atributo MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105750261"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="d51b2-104">atributo requestedit</span><span class="sxs-lookup"><span data-stu-id="d51b2-104">requestedit attribute</span></span>

<span data-ttu-id="d51b2-105">O atributo **\[ \] requestedit** indica que a propriedade dá suporte à notificação **OnRequestEdit** .</span><span class="sxs-lookup"><span data-stu-id="d51b2-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="d51b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d51b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d51b2-107">*opcional-atributos*</span><span class="sxs-lookup"><span data-stu-id="d51b2-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d51b2-108">Zero ou mais atributos MIDL.</span><span class="sxs-lookup"><span data-stu-id="d51b2-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d51b2-109">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="d51b2-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d51b2-110">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="d51b2-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="d51b2-111">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="d51b2-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d51b2-112">Especifica o nome da função no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d51b2-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="d51b2-113">*params*</span><span class="sxs-lookup"><span data-stu-id="d51b2-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="d51b2-114">Zero ou mais parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="d51b2-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d51b2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d51b2-115">Remarks</span></span>

<span data-ttu-id="d51b2-116">O suporte à notificação **OnRequestEdit** significa que, antes que uma alteração seja feita, o objeto enviará ao cliente uma solicitação de permissão para alterar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="d51b2-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="d51b2-117">Um objeto pode dar suporte à ligação de dados, mas não tem esse atributo.</span><span class="sxs-lookup"><span data-stu-id="d51b2-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="d51b2-118">Flags</span><span class="sxs-lookup"><span data-stu-id="d51b2-118">Flags</span></span>

<span data-ttu-id="d51b2-119">FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT</span><span class="sxs-lookup"><span data-stu-id="d51b2-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="d51b2-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d51b2-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="d51b2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d51b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51b2-122">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="d51b2-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="d51b2-123">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d51b2-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d51b2-124">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d51b2-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d51b2-125">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="d51b2-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 