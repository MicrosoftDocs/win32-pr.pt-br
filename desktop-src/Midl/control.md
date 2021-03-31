---
title: atributo de controle
description: O atributo \ Control \ identifica uma coclass ou biblioteca como um controle COM, do qual um site de contêiner derivará bibliotecas de tipos adicionais ou classes de objeto de componente.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- atributo de controle MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640513"
---
# <a name="control-attribute"></a><span data-ttu-id="2c41b-104">atributo de controle</span><span class="sxs-lookup"><span data-stu-id="2c41b-104">control attribute</span></span>

<span data-ttu-id="2c41b-105">O atributo **\[ Control \]** identifica uma [**coclass**](coclass.md) ou [**biblioteca**](library.md) como um controle com, da qual um site de contêiner derivará bibliotecas de tipo adicionais ou classes de objeto de componente.</span><span class="sxs-lookup"><span data-stu-id="2c41b-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="2c41b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c41b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c41b-107">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="2c41b-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41b-108">Especifica zero ou mais atributos que se aplicam à [**biblioteca**](library.md) ou à instrução [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="2c41b-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="2c41b-109">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2c41b-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="2c41b-110">*lib-ou-Coclassname*</span><span class="sxs-lookup"><span data-stu-id="2c41b-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41b-111">Especifica o nome da [**biblioteca**](library.md) ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="2c41b-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c41b-112">*definições*</span><span class="sxs-lookup"><span data-stu-id="2c41b-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="2c41b-113">Instruções MIDL que especificam os membros da [**biblioteca**](library.md) ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="2c41b-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c41b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c41b-114">Remarks</span></span>

<span data-ttu-id="2c41b-115">Esse atributo permite marcar bibliotecas de tipos que descrevem controles para que não sejam exibidas em navegadores de tipos destinados a objetos não visuais.</span><span class="sxs-lookup"><span data-stu-id="2c41b-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="2c41b-116">Flags</span><span class="sxs-lookup"><span data-stu-id="2c41b-116">Flags</span></span>

<span data-ttu-id="2c41b-117">TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL</span><span class="sxs-lookup"><span data-stu-id="2c41b-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="2c41b-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c41b-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="2c41b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c41b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c41b-120">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="2c41b-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="2c41b-121">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="2c41b-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="2c41b-122">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="2c41b-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="2c41b-123">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="2c41b-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="2c41b-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="2c41b-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="2c41b-125">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="2c41b-125">**library**</span></span>](library.md)
</dt> </dl>

 

 