---
title: atributo de intervalo
description: O atributo \ Range \ permite especificar um intervalo de valores permitidos para argumentos ou campos cujos valores são definidos em tempo de execução. Quando usado com um tipo de pipe, o atributo especifica o intervalo permitido para a contagem de elementos nas partes do pipe.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- atributo de intervalo MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105787511"
---
# <a name="range-attribute"></a><span data-ttu-id="f3754-105">atributo de intervalo</span><span class="sxs-lookup"><span data-stu-id="f3754-105">range attribute</span></span>

<span data-ttu-id="f3754-106">O atributo **\[ Range \]** permite especificar um intervalo de valores permitidos para argumentos ou campos cujos valores são definidos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f3754-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="f3754-107">Quando usado com um tipo de pipe, o atributo especifica o intervalo permitido para a contagem de elementos nas partes do pipe.</span><span class="sxs-lookup"><span data-stu-id="f3754-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="f3754-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3754-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3754-109">*valor baixo*</span><span class="sxs-lookup"><span data-stu-id="f3754-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="f3754-110">O menor valor permitido que o parâmetro ou campo pode conter.</span><span class="sxs-lookup"><span data-stu-id="f3754-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="f3754-111">*valor alto*</span><span class="sxs-lookup"><span data-stu-id="f3754-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="f3754-112">O valor mais alto permitido que o parâmetro ou campo pode conter.</span><span class="sxs-lookup"><span data-stu-id="f3754-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="f3754-113">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="f3754-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f3754-114">Um tipo integral diferente de [**Hyper**](hyper.md) ou [**\_ \_ Int64**](--int64.md), um identificador de tipo para um tipo integral, um tipo de [**Enumeração**](enum.md) ou um nome de tipo de pipe.</span><span class="sxs-lookup"><span data-stu-id="f3754-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="f3754-115">*Declarador*</span><span class="sxs-lookup"><span data-stu-id="f3754-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="f3754-116">Um Declarador C padrão, como um identificador.</span><span class="sxs-lookup"><span data-stu-id="f3754-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3754-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3754-117">Remarks</span></span>

<span data-ttu-id="f3754-118">Use o atributo **\[ Range \]** para modificar o significado de parâmetros ou campos confidenciais, como aqueles usados para tamanho ou comprimento, com matrizes em conformidade ou variáveis; ou sempre que desejar verificar um parâmetro ou valor de campo em relação a um intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="f3754-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="f3754-119">O atributo é aplicável a parâmetros de nível superior, bem como a parâmetros e campos de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="f3754-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="f3754-120">A adição do atributo **\[ Range \]** a um tipo não altera seu formato de conexão, portanto, não afeta a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f3754-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="f3754-121">O atributo **\[ Range \]** também pode ser usado em dados em conformidade, como buffers ou matrizes com um atributo de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="f3754-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="f3754-122">O efeito é limitar todos os tamanhos de conformidade para os dados de acordo com o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="f3754-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="f3754-123">Se os dados em conformidade forem uma matriz multidimensional, cada dimensão de matriz será limitada ao intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="f3754-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="f3754-124">O uso do **\[ intervalo \]** em dados em conformidade requer que o destino de compilação seja â € "Target NT60 ou superior.</span><span class="sxs-lookup"><span data-stu-id="f3754-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="f3754-125">Observe que você deve usar a opção de compilador [**/robust**](-robust.md) ao compilar o arquivo IDL para gerar o código de stub que executará essas verificações.</span><span class="sxs-lookup"><span data-stu-id="f3754-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="f3754-126">Sem a opção **/robust** , o compilador MIDL ignora esse atributo.</span><span class="sxs-lookup"><span data-stu-id="f3754-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="f3754-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3754-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="f3754-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3754-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3754-129">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="f3754-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f3754-130">matrizes</span><span class="sxs-lookup"><span data-stu-id="f3754-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="f3754-131">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="f3754-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="f3754-132">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="f3754-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="f3754-133">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="f3754-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="f3754-134">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="f3754-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="f3754-135">**/robust**</span><span class="sxs-lookup"><span data-stu-id="f3754-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="f3754-136">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="f3754-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="f3754-137">**switch \_ é**</span><span class="sxs-lookup"><span data-stu-id="f3754-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 