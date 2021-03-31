---
title: atributo in
description: O atributo \ in \ indica que um parâmetro deve ser passado do procedimento de chamada para o procedimento chamado.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- no atributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641016"
---
# <a name="in-attribute"></a><span data-ttu-id="80c4d-104">atributo in</span><span class="sxs-lookup"><span data-stu-id="80c4d-104">in attribute</span></span>

<span data-ttu-id="80c4d-105">O atributo **\[ in \]** indica que um parâmetro deve ser passado do procedimento de chamada para o procedimento chamado.</span><span class="sxs-lookup"><span data-stu-id="80c4d-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="80c4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80c4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c4d-107">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="80c4d-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="80c4d-108">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="80c4d-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="80c4d-109">Os atributos de função válidos são **\[ retorno de chamada \]**, **\[ local \]**, **\[ referência \]** de atributo de ponteiro, **\[ exclusivo \]** ou **\[ PTR \]**, e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ identificador \] de contexto**.</span><span class="sxs-lookup"><span data-stu-id="80c4d-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-110">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="80c4d-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="80c4d-111">Especifica um tipo de **base \_**, [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="80c4d-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="80c4d-112">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="80c4d-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-113">*Declarador de ponteiro*</span><span class="sxs-lookup"><span data-stu-id="80c4d-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="80c4d-114">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="80c4d-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="80c4d-115">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="80c4d-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-116">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="80c4d-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="80c4d-117">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="80c4d-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-118">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="80c4d-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="80c4d-119">Especifica zero ou mais atributos apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="80c4d-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="80c4d-120">Atributos de parâmetro com o atributo **\[ \] in** também podem pegar o atributo direcional **\[ out \]**; os atributos de campo **\[ First \_ são \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ Size \_ is \]** e **\[ switch \_ Type \]**; o atributo ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ identificador \] de contexto** e a cadeia de **\[ caracteres \]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="80c4d-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="80c4d-121">O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="80c4d-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="80c4d-122">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="80c4d-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-123">*Declarador*</span><span class="sxs-lookup"><span data-stu-id="80c4d-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="80c4d-124">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="80c4d-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="80c4d-125">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="80c4d-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="80c4d-126">O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.</span><span class="sxs-lookup"><span data-stu-id="80c4d-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80c4d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="80c4d-127">Remarks</span></span>

<span data-ttu-id="80c4d-128">O atributo in tem um atributo **\[ \] de** inverso **\[** [**,**](out-idl.md) **\]** que indica que um parâmetro deve ser retornado do procedimento chamado para o procedimento de chamada.</span><span class="sxs-lookup"><span data-stu-id="80c4d-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="80c4d-129">Os atributos in e **\[ out \]** são conhecidos como atributos **\[ de \]** parâmetro direcional, pois especificam a direção em que os parâmetros são passados.</span><span class="sxs-lookup"><span data-stu-id="80c4d-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="80c4d-130">Um parâmetro pode ser definido como **\[ in \]**, **\[ out \]** ou **\[ in**, **out \]**.</span><span class="sxs-lookup"><span data-stu-id="80c4d-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="80c4d-131">O atributo **\[ in \]** identifica parâmetros que são empacotados pelo stub do cliente para transmissão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="80c4d-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="80c4d-132">O atributo in é aplicado a um parâmetro por padrão quando nenhum atributo **\[ de \]** parâmetro direcional é especificado.</span><span class="sxs-lookup"><span data-stu-id="80c4d-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="80c4d-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80c4d-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="80c4d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="80c4d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c4d-135">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="80c4d-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="80c4d-136">**\_alocar usuário de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="80c4d-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="80c4d-137">**fora**</span><span class="sxs-lookup"><span data-stu-id="80c4d-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 