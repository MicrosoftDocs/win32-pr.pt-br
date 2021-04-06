---
title: atributo de codificação
description: O atributo \ Encode \ ACF especifica que um procedimento ou um tipo de dados precisa de suporte de serialização.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- atributo de codificação MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917184"
---
# <a name="encode-attribute"></a><span data-ttu-id="f9a95-104">atributo de codificação</span><span class="sxs-lookup"><span data-stu-id="f9a95-104">encode attribute</span></span>

<span data-ttu-id="f9a95-105">O atributo **\[ Encode \]** ACF especifica que um procedimento ou um tipo de dados precisa de suporte de serialização.</span><span class="sxs-lookup"><span data-stu-id="f9a95-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="f9a95-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9a95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a95-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="f9a95-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-108">Especifica outros atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="f9a95-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="f9a95-109">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="f9a95-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-110">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="f9a95-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="f9a95-111">*interface-definição*</span><span class="sxs-lookup"><span data-stu-id="f9a95-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-112">Especifica as instruções IDL que formam a definição da interface.</span><span class="sxs-lookup"><span data-stu-id="f9a95-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="f9a95-113">*lista de atributos de op*</span><span class="sxs-lookup"><span data-stu-id="f9a95-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-114">Especifica outros atributos operacionais que se aplicam ao procedimento como **\[** [**decodificar**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f9a95-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f9a95-115">*proc-nome*</span><span class="sxs-lookup"><span data-stu-id="f9a95-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-116">Especifica o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="f9a95-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f9a95-117">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="f9a95-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-118">Especifica outros atributos que se aplicam ao tipo, como **\[** [**decodificar**](decode.md) **\]** e **\[** [**alocar**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f9a95-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f9a95-119">*nome do tipo*</span><span class="sxs-lookup"><span data-stu-id="f9a95-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a95-120">Especifica um tipo definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f9a95-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9a95-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9a95-121">Remarks</span></span>

<span data-ttu-id="f9a95-122">O atributo de **\[ codificação \]** faz com que o compilador MIDL gere código que um aplicativo pode usar para serializar dados em um buffer.</span><span class="sxs-lookup"><span data-stu-id="f9a95-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="f9a95-123">O **\[** atributo [**decodificar**](decode.md) **\]** gera o código para desempacotamento de dados de um buffer.</span><span class="sxs-lookup"><span data-stu-id="f9a95-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="f9a95-124">Use os atributos de **\[ codificação \]** e **\[** [**decodificação**](decode.md) **\]** em um ACF para gerar código de SERIALIZAÇÃO para procedimentos ou tipos definidos no arquivo IDL de uma interface.</span><span class="sxs-lookup"><span data-stu-id="f9a95-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="f9a95-125">Quando usado como um atributo de interface, a **\[ codificação \]** se aplica a todos os tipos e procedimentos definidos no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f9a95-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="f9a95-126">Quando usado como um atributo operacional, a **\[ codificação \]** se aplica somente ao procedimento especificado.</span><span class="sxs-lookup"><span data-stu-id="f9a95-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="f9a95-127">Quando usado como um atributo de tipo, a **\[ codificação \]** se aplica somente ao tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="f9a95-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="f9a95-128">Quando o atributo de **\[ \] codificação** ou **\[** [**decodificação**](decode.md) **\]** é aplicado a um procedimento, o compilador MIDL gera um stub de serialização de maneira semelhante à medida que os stubs remotos são gerados para rotinas remotas.</span><span class="sxs-lookup"><span data-stu-id="f9a95-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="f9a95-129">Um procedimento pode ser um procedimento remoto ou de serialização, mas não pode ser ambos.</span><span class="sxs-lookup"><span data-stu-id="f9a95-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="f9a95-130">O protótipo da rotina gerada é enviado para o STUB. O arquivo H, enquanto o próprio stub entra no \_ arquivo de stub c. c.</span><span class="sxs-lookup"><span data-stu-id="f9a95-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="f9a95-131">O compilador MIDL gera duas funções para cada tipo ao qual o atributo de **\[ codificação \]** se aplica e uma função adicional para cada tipo ao qual o atributo de **\[** [**decodificação**](decode.md) **\]** se aplica.</span><span class="sxs-lookup"><span data-stu-id="f9a95-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="f9a95-132">Por exemplo, para um tipo definido pelo usuário chamado com MyType, o compilador gera código para as \_ funções com MyType Encode, com MyType \_ decodificar e com MyType \_ AlignSize.</span><span class="sxs-lookup"><span data-stu-id="f9a95-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="f9a95-133">Para essas funções, o compilador grava protótipos no STUB. H e código-fonte para \_ C.C. de stub</span><span class="sxs-lookup"><span data-stu-id="f9a95-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="f9a95-134">Para obter informações adicionais sobre identificadores de serialização e codificação ou decodificação de dados, consulte [serviços de serialização](/windows/desktop/Rpc/serialization-services).</span><span class="sxs-lookup"><span data-stu-id="f9a95-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="f9a95-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9a95-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="f9a95-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9a95-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a95-137">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="f9a95-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="f9a95-138">**aloca**</span><span class="sxs-lookup"><span data-stu-id="f9a95-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="f9a95-139">**RET**</span><span class="sxs-lookup"><span data-stu-id="f9a95-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 