---
title: atributo typedef
description: A palavra-chave de typedef IDL permite declarações de TypeDef que são muito semelhantes às declarações de typedef de linguagem C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- atributo de typedef MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640560"
---
# <a name="typedef-attribute"></a><span data-ttu-id="7e4b8-104">atributo typedef</span><span class="sxs-lookup"><span data-stu-id="7e4b8-104">typedef attribute</span></span>

<span data-ttu-id="7e4b8-105">A palavra-chave de **TYPEDEF** IDL permite declarações de **typedef** que são muito semelhantes às declarações de **typedef** de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="7e4b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e4b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e4b8-107">*IDL-tipo-atributo-List*</span><span class="sxs-lookup"><span data-stu-id="7e4b8-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7e4b8-108">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="7e4b8-109">Atributos de tipo válidos em um arquivo IDL incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7e4b8-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="7e4b8-110">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="7e4b8-111">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="7e4b8-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7e4b8-112">Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="7e4b8-113">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="7e4b8-114">A palavra-chave [**const**](const.md) pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="7e4b8-115">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="7e4b8-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7e4b8-116">Especifica declaradores de MIDL padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="7e4b8-117">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="7e4b8-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="7e4b8-118">A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="7e4b8-119">*ACF-tipo-atributo-List*</span><span class="sxs-lookup"><span data-stu-id="7e4b8-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7e4b8-120">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="7e4b8-121">Atributos de tipo válidos em um ACF incluem **\[** [**alocar**](allocate.md) **\]** , **\[** [**codificar**](encode.md) **\]** e **\[** [**decodificar**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7e4b8-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7e4b8-122">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="7e4b8-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="7e4b8-123">Especifica um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e4b8-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e4b8-124">Remarks</span></span>

<span data-ttu-id="7e4b8-125">A declaração de **typedef** de IDL é aumentada para permitir que você associe atributos de tipo aos tipos definidos.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="7e4b8-126">Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7e4b8-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="7e4b8-127">A palavra-chave **typedef** em um ACF aplica atributos a tipos que são definidos no arquivo IDL correspondente.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="7e4b8-128">Por exemplo, o atributo [**alocar**](allocate.md) tipo permite que você personalize a alocação de memória e a desalocação pelo aplicativo e pelos stubs.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="7e4b8-129">A instrução de **typedef** de ACF aparece como parte do corpo de ACF.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="7e4b8-130">Observe que a sintaxe de **typedef** de ACF é diferente da sintaxe de **typedef** de IDL e da sintaxe de **typedef** de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="7e4b8-131">Nenhum tipo novo pode ser introduzido no ACF.</span><span class="sxs-lookup"><span data-stu-id="7e4b8-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e4b8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e4b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e4b8-133">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="7e4b8-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-134">**aloca**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-135">**Storage**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-136">**const**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-137">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-138">**RET**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-139">**codificado**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-140">**enumera**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-141">**processamento**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-142">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="7e4b8-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-143">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-146">**string**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-147">**struct**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-148">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-149">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-150">**unida**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="7e4b8-151">**diferente**</span><span class="sxs-lookup"><span data-stu-id="7e4b8-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 