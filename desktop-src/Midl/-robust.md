---
title: comutador/robust
description: A opção/robust informa o compilador MIDL para gerar informações adicionais de verificação de erros, que o mecanismo de NDR usa para executar verificações de integridade em tempo de execução.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- MIDL do comutador/robust
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823179"
---
# <a name="robust-switch"></a><span data-ttu-id="88d37-104">comutador/robust</span><span class="sxs-lookup"><span data-stu-id="88d37-104">/robust switch</span></span>

<span data-ttu-id="88d37-105">A opção **/robust** informa o compilador MIDL para gerar informações adicionais de verificação de erros, que o mecanismo de NDR usa para executar verificações de integridade em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="88d37-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="88d37-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="88d37-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="88d37-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="88d37-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="88d37-108">*/OIF*</span><span class="sxs-lookup"><span data-stu-id="88d37-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="88d37-109">Essas opções são idênticas em sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="88d37-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="88d37-110">Eles especificam o método de proxy com código de marshaling e usam cadeias de caracteres de formato rápido para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="88d37-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="88d37-111">Consulte/ [**Oi**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="88d37-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88d37-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="88d37-112">Remarks</span></span>

<span data-ttu-id="88d37-113">O uso da opção **/robust** gera informações adicionais que permitem que o mecanismo de representação de dados de rede (NDR) execute a verificação de erros em tempo de execução em argumentos correlacionados em matrizes dinâmicas, uniões e ponteiros [**de interface em**](out-idl.md) aplicativos DCOM.</span><span class="sxs-lookup"><span data-stu-id="88d37-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="88d37-114">A opção **/robust** só está disponível no WindowsÂ 2000 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="88d37-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="88d37-115">Um argumento correlacionado é um argumento que usa qualquer um dos atributos que permitem que o tamanho de um objeto de dados seja determinado em tempo de execução: o [**tamanho \_ é**](size-is.md), o [**comprimento \_ é**](length-is.md), o [**primeiro \_ é**](first-is.md), o [**último \_ é**](last-is.md), o [**máximo \_ é**](max-is.md), o [**switch \_ é**](switch-is.md)e o [**IID \_ é**](iid-is.md).</span><span class="sxs-lookup"><span data-stu-id="88d37-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="88d37-116">De acordo com a especificação uso-DCE para a representação de transmissão, esse argumento correlacionado aparece em dois locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="88d37-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="88d37-117">Por exemplo, considere um uso típico do **tamanho como \_** atributo:</span><span class="sxs-lookup"><span data-stu-id="88d37-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="88d37-118">Neste exemplo, o cliente passa um Long que especifica o tamanho de um bloco de tipos de barra \_ (em termos de número de elementos de tipos de barra \_ ) e um ponteiro para o bloco real de \_ tipos de barra.</span><span class="sxs-lookup"><span data-stu-id="88d37-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="88d37-119">O argumento size se correlaciona com o argumento pBarType.</span><span class="sxs-lookup"><span data-stu-id="88d37-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="88d37-120">De acordo com a especificação uso-DCE, o argumento Size é representado duas vezes na transmissão, primeiro como em si e, em seguida, com a matriz de elementos de tipo de barra \_ que representam o argumento pBarType.</span><span class="sxs-lookup"><span data-stu-id="88d37-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="88d37-121">Cada argumento é desempacotado de forma independente, de acordo com sua própria representação de conexão.</span><span class="sxs-lookup"><span data-stu-id="88d37-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="88d37-122">Normalmente, o argumento size e sua cópia, que é usada para representar parte do outro argumento, têm os mesmos valores.</span><span class="sxs-lookup"><span data-stu-id="88d37-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="88d37-123">No entanto, se o argumento de tamanho se tornar corrompido (por exemplo, quando o bloco de tipos de barra \_ for maior do que o que foi alocado), o aplicativo de servidor poderá parar de responder, pois ele usa o valor do argumento size para medir os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="88d37-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="88d37-124">A opção **/robust** é necessária para implementar a verificação de intervalo válida com o atributo [**Range**](range.md) .</span><span class="sxs-lookup"><span data-stu-id="88d37-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="88d37-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88d37-125">Examples</span></span>

<span data-ttu-id="88d37-126">**MIDL/robust/Oicf filename. idl**</span><span class="sxs-lookup"><span data-stu-id="88d37-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="88d37-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="88d37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d37-128">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="88d37-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="88d37-129">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="88d37-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="88d37-130">**amplitude**</span><span class="sxs-lookup"><span data-stu-id="88d37-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




