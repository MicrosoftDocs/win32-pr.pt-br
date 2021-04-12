---
title: atributo de proxy
description: O atributo \ proxy \ impede que a automação se registre como um manipulador de proxy/stub para uma interface dupla.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- atributo proxy MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453975"
---
# <a name="proxy-attribute"></a><span data-ttu-id="82c6e-104">atributo de proxy</span><span class="sxs-lookup"><span data-stu-id="82c6e-104">proxy attribute</span></span>

<span data-ttu-id="82c6e-105">O atributo **\[ proxy \]** impede que a automação se registre como um manipulador de proxy/stub para uma interface dupla.</span><span class="sxs-lookup"><span data-stu-id="82c6e-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="82c6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82c6e-107">*Cadeia de caracteres-UUID*</span><span class="sxs-lookup"><span data-stu-id="82c6e-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="82c6e-108">Especifica uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen, em seguida, três grupos de quatro dígitos hexadecimais, cada um seguido por um hífen e 12 dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="82c6e-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="82c6e-109">Você pode colocar a cadeia de caracteres UUID entre aspas, exceto quando você usar o [**/OSF**](-osf.md)do compilador MIDL switch.</span><span class="sxs-lookup"><span data-stu-id="82c6e-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="82c6e-110">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="82c6e-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="82c6e-111">Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="82c6e-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="82c6e-112">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="82c6e-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="82c6e-113">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="82c6e-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="82c6e-114">Nome da interface.</span><span class="sxs-lookup"><span data-stu-id="82c6e-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="82c6e-115">*interface base*</span><span class="sxs-lookup"><span data-stu-id="82c6e-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="82c6e-116">Especifica o nome de uma interface da qual essa interface derivada herda funções de membro, códigos de status e atributos de interface.</span><span class="sxs-lookup"><span data-stu-id="82c6e-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="82c6e-117">A interface derivada não herda definições de tipo.</span><span class="sxs-lookup"><span data-stu-id="82c6e-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="82c6e-118">Para fazer isso, use a palavra-chave [**Import**](import.md) para importar o arquivo IDL da interface base.</span><span class="sxs-lookup"><span data-stu-id="82c6e-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82c6e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="82c6e-119">Remarks</span></span>

<span data-ttu-id="82c6e-120">O uso do \[  \] atributo proxy para uma interface dupla impede que o tlb assuma os stubs gerados.</span><span class="sxs-lookup"><span data-stu-id="82c6e-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="82c6e-121">Se esse atributo for especificado, o proxy de TypeLib não deverá ter o registro cancelado quando o registro de typelib tiver sido cancelado.</span><span class="sxs-lookup"><span data-stu-id="82c6e-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="82c6e-122">Flags</span><span class="sxs-lookup"><span data-stu-id="82c6e-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="82c6e-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="82c6e-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="82c6e-124">As interfaces podem ser marcadas com o \_ sinalizador de proxy TYPEFLAG para indicar que estarão usando uma biblioteca de vínculo dinâmico de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="82c6e-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="82c6e-125">Esse sinalizador especifica que o proxy de TypeLib não deve ter o registro cancelado quando o typelib tem o registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="82c6e-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="82c6e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="82c6e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c6e-127">**Gerando uma biblioteca de tipos com MIDL**</span><span class="sxs-lookup"><span data-stu-id="82c6e-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="82c6e-128">**simplifica**</span><span class="sxs-lookup"><span data-stu-id="82c6e-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="82c6e-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="82c6e-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 