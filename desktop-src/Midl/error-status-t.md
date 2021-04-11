---
title: error_status_t atributo
description: A \_ \_ palavra-chave status de erro t designa um tipo para um objeto que contém informações de status de comunicação ou de status de falha.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t do atributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293085"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="ba389-104">\_atributo t de status de erro \_</span><span class="sxs-lookup"><span data-stu-id="ba389-104">error\_status\_t attribute</span></span>

<span data-ttu-id="ba389-105">A palavra-chave **status de erro \_ \_ t** designa um tipo para um objeto que contém informações de status de comunicação ou de status de falha.</span><span class="sxs-lookup"><span data-stu-id="ba389-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="ba389-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba389-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba389-107">*ACF-função-atributos*</span><span class="sxs-lookup"><span data-stu-id="ba389-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ba389-108">Especifica zero ou mais atributos de função de ACF, como **\[** [**\_ status de comunicação**](comm-status.md) **\]** , **\[** [**\_ status de falha**](fault-status.md) **\]** ou **\[** [**Nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ba389-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="ba389-109">Os atributos de função são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="ba389-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ba389-110">Zero ou mais atributos podem ser aplicados a uma função.</span><span class="sxs-lookup"><span data-stu-id="ba389-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="ba389-111">Separe vários atributos de função com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="ba389-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ba389-112">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="ba389-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ba389-113">Especifica o nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="ba389-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="ba389-114">*ACF-parâmetros-atributos*</span><span class="sxs-lookup"><span data-stu-id="ba389-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ba389-115">Especifica os atributos que se aplicam a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba389-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="ba389-116">Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba389-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="ba389-117">Separe vários atributos de parâmetro com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="ba389-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="ba389-118">Os atributos de parâmetro são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="ba389-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ba389-119">Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF.</span><span class="sxs-lookup"><span data-stu-id="ba389-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="ba389-120">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="ba389-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ba389-121">Especifica o parâmetro para a função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="ba389-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="ba389-122">Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="ba389-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba389-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba389-123">Remarks</span></span>

<span data-ttu-id="ba389-124">O **tipo \_ \_ t de status de erro** é usado como parte da arquitetura de tratamento de exceção em IDL.</span><span class="sxs-lookup"><span data-stu-id="ba389-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="ba389-125">Esse tipo é mapeado para um [**longo**](long.md) [**não assinado**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="ba389-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="ba389-126">Os aplicativos que capturam situações de erro têm um **\[** parâmetro [**out**](out-idl.md) **\]** ou um tipo de retorno de um procedimento especificado como **status de erro \_ \_ t** e qualificam o **status de erro \_ \_ t** com os **\[** atributos [**\_ status de comunicação**](comm-status.md) **\]** ou **\[** [**\_ status de falha**](fault-status.md) **\]** no ACF.</span><span class="sxs-lookup"><span data-stu-id="ba389-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="ba389-127">Se o parâmetro ou tipo de retorno não tiver sido qualificado com os atributos **\[ \_ status \] de comunicação** ou **\[ \_ status \] de falha** , o parâmetro funcionará como se fosse um longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="ba389-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="ba389-128">A partir da versão 2,0, o compilador MIDL gera stubs que contêm a arquitetura de tratamento de erros apropriada.</span><span class="sxs-lookup"><span data-stu-id="ba389-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="ba389-129">No entanto, as versões anteriores do compilador MIDL trataram um parâmetro ou um tipo de retorno de **status de erro \_ \_ t** , como se os atributos status de **\[** [**comunicação \_**](comm-status.md) **\]** e **\[** [**\_ status de falha**](fault-status.md) **\]** fossem aplicados, mesmo que eles não fossem.</span><span class="sxs-lookup"><span data-stu-id="ba389-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="ba389-130">Com o MIDL 2,0 ou posterior, você deve aplicar explicitamente os atributos **\[ \_ status \] de comunicação** e **\[ \_ status \] de falha** ao parâmetro ou procedimento no ACF.</span><span class="sxs-lookup"><span data-stu-id="ba389-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="ba389-131">O tipo de **status de erro \_ \_ t** é um dos tipos predefinidos da linguagem de definição de interface.</span><span class="sxs-lookup"><span data-stu-id="ba389-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="ba389-132">Tipos predefinidos podem aparecer como especificadores de tipo em declarações de [**typedef**](typedef.md) , em declarações gerais e em declaradores de função (como o tipo de retorno de função ou como especificadores de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="ba389-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="ba389-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba389-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba389-134">**status de comunicação \_**</span><span class="sxs-lookup"><span data-stu-id="ba389-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="ba389-135">**status de falha \_**</span><span class="sxs-lookup"><span data-stu-id="ba389-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="ba389-136">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ba389-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ba389-137">**Longas**</span><span class="sxs-lookup"><span data-stu-id="ba389-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="ba389-138">**fora**</span><span class="sxs-lookup"><span data-stu-id="ba389-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ba389-139">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ba389-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="ba389-140">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="ba389-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




