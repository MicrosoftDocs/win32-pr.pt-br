---
title: Técnicas de IDL para melhor design de interface e de método
description: Considere o uso das seguintes técnicas específicas de IDL para melhorar a segurança e o desempenho quando você estiver desenvolvendo interfaces e métodos de RPC que lidam com dados de variante e em conformidade.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363919"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a><span data-ttu-id="b6ade-103">Técnicas de IDL para melhor design de interface e de método</span><span class="sxs-lookup"><span data-stu-id="b6ade-103">IDL Techniques for Better Interface and Method Design</span></span>

<span data-ttu-id="b6ade-104">Considere o uso das seguintes técnicas específicas de IDL para melhorar a segurança e o desempenho quando você estiver desenvolvendo interfaces e métodos de RPC que lidam com dados de variante e em conformidade.</span><span class="sxs-lookup"><span data-stu-id="b6ade-104">Consider using the following IDL-specific techniques to improve security and performance when you are developing RPC interfaces and methods that handle both conformant and variant data.</span></span> <span data-ttu-id="b6ade-105">Os atributos mencionados neste tópico são os atributos IDL definidos nos parâmetros do método que lidam com dados de conformidade (por exemplo, o \[ **tamanho \_** \] e o \[ **máximo \_ são** \] atributos) ou dados variantes (por exemplo, o \[ **comprimento \_ é** \] e \[ atributos de cadeia de **caracteres** \] ).</span><span class="sxs-lookup"><span data-stu-id="b6ade-105">The attributes referred to in this topic are the IDL attributes set on method parameters that handle either conformant data (for example, the \[**size\_is**\] and \[**max\_is**\] attributes) or variant data (for example, the \[**length\_is**\] and \[**string**\] attributes).</span></span>

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a><span data-ttu-id="b6ade-106">Usando o \[ \] atributo Range com parâmetros de dados em conformidade</span><span class="sxs-lookup"><span data-stu-id="b6ade-106">Using the \[range\] Attribute with Conformant Data Parameters</span></span>

<span data-ttu-id="b6ade-107">O \[  \] atributo Range instrui o tempo de execução do RPC a executar a validação de tamanho adicional durante o processo de desempacotamento de dados.</span><span class="sxs-lookup"><span data-stu-id="b6ade-107">The \[**range**\] attribute instructs the RPC run-time to perform additional size validation during the data unmarshaling process.</span></span> <span data-ttu-id="b6ade-108">Especificamente, ele verifica se o tamanho fornecido dos dados passados como o parâmetro associado está dentro do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="b6ade-108">Specifically, it verifies that the supplied size of the data passed as the associated parameter is within the specified range.</span></span>

<span data-ttu-id="b6ade-109">O \[ atributo de **intervalo** \] não afeta o formato de conexão.</span><span class="sxs-lookup"><span data-stu-id="b6ade-109">The \[**range**\] attribute does not affect wire format.</span></span>

<span data-ttu-id="b6ade-110">Se o valor na conexão estiver fora do intervalo permitido, o RPC lançará uma exceção de dados de stub de RPC \_ x \_ inválida \_ ou de RPC \_ x inválido \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b6ade-110">If the value on wire is outside of the allowed range, RPC will throw an RPC\_X\_INVALID\_BOUND or RPC\_X\_BAD\_STUB\_DATA exception.</span></span> <span data-ttu-id="b6ade-111">Isso fornece um nível adicional de validação de dados e pode ajudar a evitar erros comuns de segurança, como saturações de buffer.</span><span class="sxs-lookup"><span data-stu-id="b6ade-111">This provides an additional level of data validation, and can help prevent common security errors like buffer overruns.</span></span> <span data-ttu-id="b6ade-112">Da mesma forma, o uso do \[ **intervalo** \] pode melhorar o desempenho do aplicativo, pois os dados em conformidade marcados com ele têm restrições claramente definidas disponíveis para consideração pelo serviço RPC.</span><span class="sxs-lookup"><span data-stu-id="b6ade-112">Likewise, using \[**range**\] can improve application performance, since conformant data marked with it has clearly-defined constraints available for consideration by the RPC service.</span></span>

## <a name="rpc-server-stub-memory-management-rules"></a><span data-ttu-id="b6ade-113">Regras de gerenciamento de memória de stub do servidor RPC</span><span class="sxs-lookup"><span data-stu-id="b6ade-113">RPC Server Stub Memory Management Rules</span></span>

<span data-ttu-id="b6ade-114">É importante entender as regras de gerenciamento de memória de stub do servidor RPC ao criar os arquivos IDL para um aplicativo habilitado para RPC.</span><span class="sxs-lookup"><span data-stu-id="b6ade-114">It is important to understand RPC server stub memory management rules when creating the IDL files for an RPC-enabled application.</span></span> <span data-ttu-id="b6ade-115">Os aplicativos podem melhorar a utilização de recursos do servidor usando \[ **Range** \] em conjunto com dados em conformidade, conforme indicado acima, bem como evitar deliberadamente a aplicação de atributos IDL de dados de comprimento variável, como \[ **comprimento, \_ é** \] para os dados em conformidade.</span><span class="sxs-lookup"><span data-stu-id="b6ade-115">Applications can improve server resource utilization by using \[**range**\] in conjunction with conformant data as indicated above, as well as deliberately avoiding the application of variable-length data IDL attributes like like \[**length\_is**\] to conformant data.</span></span>

<span data-ttu-id="b6ade-116">O aplicativo de \[ **comprimento \_ é** \] para os campos de estrutura de dados definidos em um arquivo IDL não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="b6ade-116">The application of \[**length\_is**\] to data structure fields defined in an IDL file is not recommended.</span></span>

## <a name="best-practices-for-variable-length-data-parameters"></a><span data-ttu-id="b6ade-117">Práticas recomendadas para parâmetros de dados de comprimento variável</span><span class="sxs-lookup"><span data-stu-id="b6ade-117">Best Practices for Variable-length Data Parameters</span></span>

<span data-ttu-id="b6ade-118">Veja a seguir várias práticas recomendadas a serem consideradas ao definir os atributos IDL para estruturas de dados de tamanho variável, parâmetros de método e campos.</span><span class="sxs-lookup"><span data-stu-id="b6ade-118">The following are several best practices to consider when defining the IDL attributes for variable-sized data structures, method parameters and fields.</span></span>

-   <span data-ttu-id="b6ade-119">Use a correlação inicial.</span><span class="sxs-lookup"><span data-stu-id="b6ade-119">Use early correlation.</span></span> <span data-ttu-id="b6ade-120">Geralmente, é melhor definir o parâmetro ou o campo de tamanho da variável, de modo que ele ocorra imediatamente após o tipo integral de controle.</span><span class="sxs-lookup"><span data-stu-id="b6ade-120">It is generally better to define the variable size parameter or field such that it occurs immediately after the controlling integral type.</span></span>

    <span data-ttu-id="b6ade-121">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="b6ade-121">For example,</span></span>

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    <span data-ttu-id="b6ade-122">é melhor que</span><span class="sxs-lookup"><span data-stu-id="b6ade-122">is better than</span></span>

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    <span data-ttu-id="b6ade-123">onde **earlyCorr** declara o parâmetro de tamanho imediatamente antes do parâmetro de dados de comprimento variável e **lateCorr** declara o parâmetro de tamanho depois dele.</span><span class="sxs-lookup"><span data-stu-id="b6ade-123">wherein **earlyCorr** declares the size parameter immediately before the variable-length data parameter, and **lateCorr** declares the size parameter after it.</span></span> <span data-ttu-id="b6ade-124">O uso da correspondência inicial melhora o desempenho geral, especialmente em casos em que o método é chamado com frequência.</span><span class="sxs-lookup"><span data-stu-id="b6ade-124">Using early correspondence improves performance overall, especially in cases where the method is called frequently.</span></span>

-   <span data-ttu-id="b6ade-125">Para parâmetros marcados com \[ **out, Size \_ é** \] tupla de atributo e onde o comprimento dos dados é conhecido no lado do cliente ou em que o cliente tem um limite superior razoável, a definição do método deve ser semelhante à seguinte em termos de atribuição de parâmetro e sequência:</span><span class="sxs-lookup"><span data-stu-id="b6ade-125">For parameters marked with the \[**out, size\_is**\] attribute tuple, and where the data length is known on the client side or where the client has a reasonable upper bound, the method definition should be similar to the following in terms of parameter attribution and sequence:</span></span>

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    <span data-ttu-id="b6ade-126">Nesse caso, o cliente fornece um buffer de tamanho fixo para *pArr*, permitindo que o serviço RPC do lado do servidor aloque um buffer razoavelmente dimensionado com um bom grau de garantia.</span><span class="sxs-lookup"><span data-stu-id="b6ade-126">In this case, the client provides a fixed size buffer for *pArr*, allowing the server-side RPC service to allocate a reasonably-sized buffer with a good degree of assurance.</span></span> <span data-ttu-id="b6ade-127">Observe que, no exemplo, os dados são recebidos do servidor ( \[ **saída** \] ).</span><span class="sxs-lookup"><span data-stu-id="b6ade-127">Note that in the example the data is received from the server (\[**out**\]).</span></span> <span data-ttu-id="b6ade-128">A definição é semelhante para os dados passados para o servidor ( \[ **em** \] ).</span><span class="sxs-lookup"><span data-stu-id="b6ade-128">The definition is similar for data passed to the server (\[**in**\]).</span></span>

-   <span data-ttu-id="b6ade-129">Para situações em que o componente do lado do servidor de um aplicativo RPC decide o comprimento dos dados, a definição do método deve ser semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="b6ade-129">For situations where the server-side component of an RPC application decides the data length, the method definition should be similar to the following:</span></span>

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    <span data-ttu-id="b6ade-130">**Em \_ intervalo LONG** é um tipo definido para os stubs de cliente e de servidor e de um tamanho especificado que o cliente pode prever corretamente.</span><span class="sxs-lookup"><span data-stu-id="b6ade-130">**RANGED\_LONG** is a type defined for both the client and server stubs, and of a specified size the client can correctly anticipate.</span></span> <span data-ttu-id="b6ade-131">No exemplo, o cliente passa *ppArr* como **nulo** e o componente de aplicativo do servidor RPC aloca a quantidade correta de memória.</span><span class="sxs-lookup"><span data-stu-id="b6ade-131">In the example, the client passes *ppArr* as **NULL**, and the RPC server application component allocates the correct amount of memory.</span></span> <span data-ttu-id="b6ade-132">No retorno, o serviço RPC no lado do cliente aloca a memória para os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="b6ade-132">Upon return, the RPC service on the client side allocates the memory for the returned data.</span></span>

-   <span data-ttu-id="b6ade-133">Se o cliente quiser enviar um subconjunto de uma matriz compatível grande para o servidor, o aplicativo poderá especificar o tamanho do subconjunto, conforme demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b6ade-133">If the client wants to send a subset of a large conformant array to the server, the application can specify the size of the subset as demonstrated in the following example:</span></span>

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="b6ade-134">Dessa forma, o RPC só transmitirá os elementos *lLength* da matriz pela conexão.</span><span class="sxs-lookup"><span data-stu-id="b6ade-134">This way RPC will only transmit *lLength* elements of the array across the wire.</span></span> <span data-ttu-id="b6ade-135">No entanto, essa definição força o serviço RPC a alocar memória de tamanho *lSize* no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="b6ade-135">However, this definition forces the RPC service to allocate memory of size *lSize* on the server side.</span></span>

-   <span data-ttu-id="b6ade-136">Se o componente de aplicativo cliente determinar o tamanho máximo de uma matriz que o servidor pode retornar, mas permitir que o servidor transmita um subconjunto dessa matriz, o aplicativo poderá especificar esse comportamento definindo o IDL semelhante ao exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b6ade-136">If the client application component determines the maximum size of an array the server can return, but allows the server to transmit a subset of that array, the application can specify such a behavior by defining the IDL similar to the following example:</span></span>

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="b6ade-137">O componente de aplicativo cliente especifica o tamanho máximo da matriz e o servidor especifica quantos elementos ele transmite de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="b6ade-137">The client application component specifies the maximum size of the array, and the server specifies how many elements it transmits back to the client.</span></span>

-   <span data-ttu-id="b6ade-138">Se o componente de aplicativo do servidor precisar retornar uma cadeia de caracteres para o componente do aplicativo cliente e se o cliente souber o tamanho máximo a ser retornado do servidor, o aplicativo poderá usar um tipo de cadeia de caracteres compatível, conforme demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b6ade-138">If the server application component needs to return a string to the client application component, and if the client knows the maximum size to be returned from the server, the application can use a conformant string type as demonstrated in the following example:</span></span>

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   <span data-ttu-id="b6ade-139">Se o componente do aplicativo cliente não deve controlar o tamanho da cadeia de caracteres, o serviço RPC pode especificamente alocar a memória, conforme demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b6ade-139">If the client application component should not control the size of the string, the RPC service can specifically allocate the memory as demonstrated in the following example:</span></span>

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    <span data-ttu-id="b6ade-140">O componente de aplicativo cliente deve definir *ppStr* como **nulo** ao chamar o método RPC.</span><span class="sxs-lookup"><span data-stu-id="b6ade-140">The client application component must set *ppStr* to **NULL** on when calling the RPC method.</span></span>

 

 




