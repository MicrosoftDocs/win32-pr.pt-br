---
title: atributo de decodificação
description: O atributo \ decodificar \ ACF especifica que um procedimento ou um tipo precisa de suporte de desserialização.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- atributo de decodificação MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293983"
---
# <a name="decode-attribute"></a><span data-ttu-id="57fae-104">atributo de decodificação</span><span class="sxs-lookup"><span data-stu-id="57fae-104">decode attribute</span></span>

<span data-ttu-id="57fae-105">O atributo **\[ decodificar \]** ACF especifica que um procedimento ou um tipo precisa de suporte de desserialização.</span><span class="sxs-lookup"><span data-stu-id="57fae-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="57fae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57fae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fae-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="57fae-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-108">Especifica outros atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="57fae-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="57fae-109">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="57fae-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-110">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="57fae-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="57fae-111">*interface-definição*</span><span class="sxs-lookup"><span data-stu-id="57fae-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-112">Especifica as instruções IDL que formam a definição da interface.</span><span class="sxs-lookup"><span data-stu-id="57fae-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="57fae-113">*lista de atributos de op*</span><span class="sxs-lookup"><span data-stu-id="57fae-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-114">Especifica outros atributos operacionais que se aplicam ao procedimento, como **\[** [**Encode**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="57fae-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="57fae-115">*proc-nome*</span><span class="sxs-lookup"><span data-stu-id="57fae-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-116">Especifica o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="57fae-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="57fae-117">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="57fae-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-118">Especifica outros atributos, como **\[** [**codificar**](encode.md) **\]** e **\[** [**alocar**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="57fae-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="57fae-119">*nome do tipo*</span><span class="sxs-lookup"><span data-stu-id="57fae-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="57fae-120">Especifica um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="57fae-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57fae-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="57fae-121">Remarks</span></span>

<span data-ttu-id="57fae-122">O atributo **\[ decodificar \]** faz com que o compilador MIDL gere código que um aplicativo pode usar para recuperar dados serializados de um buffer.</span><span class="sxs-lookup"><span data-stu-id="57fae-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="57fae-123">O **\[** [](encode.md) **\]** atributo codificar fornece suporte de serialização, gerando o código para serializar dados em um buffer.</span><span class="sxs-lookup"><span data-stu-id="57fae-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="57fae-124">Use os **\[** atributos de [**codificação**](encode.md) **\]** e **\[ decodificação \]** em um ACF para gerar código de SERIALIZAÇÃO para procedimentos ou tipos definidos no arquivo IDL de uma interface.</span><span class="sxs-lookup"><span data-stu-id="57fae-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="57fae-125">Quando usado como um atributo de interface, **\[ decodificar \]** aplica-se a todos os tipos e procedimentos definidos no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="57fae-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="57fae-126">Quando usado como um atributo de tipo, **\[ decodificar \]** aplica-se somente ao tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="57fae-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="57fae-127">Quando usado como um atributo operacional, **\[ decodificar \]** aplica-se somente a esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="57fae-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="57fae-128">Para obter mais informações sobre como usar esse suporte de serialização, consulte [serialização de serviços](/windows/desktop/Rpc/serialization-services) e **\[** [**codificação**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="57fae-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="57fae-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="57fae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fae-130">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="57fae-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="57fae-131">**aloca**</span><span class="sxs-lookup"><span data-stu-id="57fae-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="57fae-132">**codificado**</span><span class="sxs-lookup"><span data-stu-id="57fae-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 