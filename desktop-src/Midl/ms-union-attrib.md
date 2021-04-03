---
title: Atributo ms_union
description: A palavra-chave \ MS \_ Union \ é usada para controlar o alinhamento de NDR de uniões não encapsuladas.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union do atributo MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006372"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="45a30-104">\_atributo Union do MS</span><span class="sxs-lookup"><span data-stu-id="45a30-104">ms\_union attribute</span></span>

<span data-ttu-id="45a30-105">A palavra-chave \[ **MS \_ Union** \] é usada para controlar o alinhamento de NDR de uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="45a30-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="45a30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45a30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45a30-107">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="45a30-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="45a30-108">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="45a30-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="45a30-109">*tipo de procedimento*</span><span class="sxs-lookup"><span data-stu-id="45a30-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="45a30-110">Especifica o tipo de retorno do procedimento ao qual o atributo está sendo aplicado.</span><span class="sxs-lookup"><span data-stu-id="45a30-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="45a30-111">*nome do procedimento*</span><span class="sxs-lookup"><span data-stu-id="45a30-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="45a30-112">Especifica o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="45a30-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="45a30-113">*parâmetro-lista*</span><span class="sxs-lookup"><span data-stu-id="45a30-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="45a30-114">Especifica a lista de parâmetros do procedimento, que pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="45a30-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45a30-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="45a30-115">Remarks</span></span>

<span data-ttu-id="45a30-116">Nunca use esta opção ou atributo com novas interfaces.</span><span class="sxs-lookup"><span data-stu-id="45a30-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="45a30-117">Este é apenas um recurso de compatibilidade com versões anteriores. O compilador MIDL nesta versão do Microsoft RPC espelha o comportamento do compilador uso DCE IDL para uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="45a30-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="45a30-118">No entanto, como as versões anteriores do compilador MIDL não faziam isso, a opção [**\_ Union/MS**](-ms-union.md) fornece compatibilidade com interfaces criadas em versões anteriores do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="45a30-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="45a30-119">O **recurso \_ Union da MS** pode ser usado como um atributo de interface IDL, um atributo de tipo IDL ou uma opção de linha de comando ( [**/MS \_ Union**](-ms-union.md)).</span><span class="sxs-lookup"><span data-stu-id="45a30-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="45a30-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45a30-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="45a30-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="45a30-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a30-122">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="45a30-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="45a30-123">**/MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="45a30-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




