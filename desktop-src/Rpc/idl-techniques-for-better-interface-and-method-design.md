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
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Técnicas de IDL para melhor design de interface e de método

Considere o uso das seguintes técnicas específicas de IDL para melhorar a segurança e o desempenho quando você estiver desenvolvendo interfaces e métodos de RPC que lidam com dados de variante e em conformidade. Os atributos mencionados neste tópico são os atributos IDL definidos nos parâmetros do método que lidam com dados de conformidade (por exemplo, o \[ **tamanho \_** \] e o \[ **máximo \_ são** \] atributos) ou dados variantes (por exemplo, o \[ **comprimento \_ é** \] e \[ atributos de cadeia de **caracteres** \] ).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Usando o \[ \] atributo Range com parâmetros de dados em conformidade

O \[  \] atributo Range instrui o tempo de execução do RPC a executar a validação de tamanho adicional durante o processo de desempacotamento de dados. Especificamente, ele verifica se o tamanho fornecido dos dados passados como o parâmetro associado está dentro do intervalo especificado.

O \[ atributo de **intervalo** \] não afeta o formato de conexão.

Se o valor na conexão estiver fora do intervalo permitido, o RPC lançará uma exceção de dados de stub de RPC \_ x \_ inválida \_ ou de RPC \_ x inválido \_ \_ \_ . Isso fornece um nível adicional de validação de dados e pode ajudar a evitar erros comuns de segurança, como saturações de buffer. Da mesma forma, o uso do \[ **intervalo** \] pode melhorar o desempenho do aplicativo, pois os dados em conformidade marcados com ele têm restrições claramente definidas disponíveis para consideração pelo serviço RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Regras de gerenciamento de memória de stub do servidor RPC

É importante entender as regras de gerenciamento de memória de stub do servidor RPC ao criar os arquivos IDL para um aplicativo habilitado para RPC. Os aplicativos podem melhorar a utilização de recursos do servidor usando \[ **Range** \] em conjunto com dados em conformidade, conforme indicado acima, bem como evitar deliberadamente a aplicação de atributos IDL de dados de comprimento variável, como \[ **comprimento, \_ é** \] para os dados em conformidade.

O aplicativo de \[ **comprimento \_ é** \] para os campos de estrutura de dados definidos em um arquivo IDL não é recomendado.

## <a name="best-practices-for-variable-length-data-parameters"></a>Práticas recomendadas para parâmetros de dados de comprimento variável

Veja a seguir várias práticas recomendadas a serem consideradas ao definir os atributos IDL para estruturas de dados de tamanho variável, parâmetros de método e campos.

-   Use a correlação inicial. Geralmente, é melhor definir o parâmetro ou o campo de tamanho da variável, de modo que ele ocorra imediatamente após o tipo integral de controle.

    Por exemplo,

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    é melhor que

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    onde **earlyCorr** declara o parâmetro de tamanho imediatamente antes do parâmetro de dados de comprimento variável e **lateCorr** declara o parâmetro de tamanho depois dele. O uso da correspondência inicial melhora o desempenho geral, especialmente em casos em que o método é chamado com frequência.

-   Para parâmetros marcados com \[ **out, Size \_ é** \] tupla de atributo e onde o comprimento dos dados é conhecido no lado do cliente ou em que o cliente tem um limite superior razoável, a definição do método deve ser semelhante à seguinte em termos de atribuição de parâmetro e sequência:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    Nesse caso, o cliente fornece um buffer de tamanho fixo para *pArr*, permitindo que o serviço RPC do lado do servidor aloque um buffer razoavelmente dimensionado com um bom grau de garantia. Observe que, no exemplo, os dados são recebidos do servidor ( \[ **saída** \] ). A definição é semelhante para os dados passados para o servidor ( \[ **em** \] ).

-   Para situações em que o componente do lado do servidor de um aplicativo RPC decide o comprimento dos dados, a definição do método deve ser semelhante à seguinte:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **Em \_ intervalo LONG** é um tipo definido para os stubs de cliente e de servidor e de um tamanho especificado que o cliente pode prever corretamente. No exemplo, o cliente passa *ppArr* como **nulo** e o componente de aplicativo do servidor RPC aloca a quantidade correta de memória. No retorno, o serviço RPC no lado do cliente aloca a memória para os dados retornados.

-   Se o cliente quiser enviar um subconjunto de uma matriz compatível grande para o servidor, o aplicativo poderá especificar o tamanho do subconjunto, conforme demonstrado no exemplo a seguir:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    Dessa forma, o RPC só transmitirá os elementos *lLength* da matriz pela conexão. No entanto, essa definição força o serviço RPC a alocar memória de tamanho *lSize* no lado do servidor.

-   Se o componente de aplicativo cliente determinar o tamanho máximo de uma matriz que o servidor pode retornar, mas permitir que o servidor transmita um subconjunto dessa matriz, o aplicativo poderá especificar esse comportamento definindo o IDL semelhante ao exemplo a seguir:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    O componente de aplicativo cliente especifica o tamanho máximo da matriz e o servidor especifica quantos elementos ele transmite de volta para o cliente.

-   Se o componente de aplicativo do servidor precisar retornar uma cadeia de caracteres para o componente do aplicativo cliente e se o cliente souber o tamanho máximo a ser retornado do servidor, o aplicativo poderá usar um tipo de cadeia de caracteres compatível, conforme demonstrado no exemplo a seguir:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Se o componente do aplicativo cliente não deve controlar o tamanho da cadeia de caracteres, o serviço RPC pode especificamente alocar a memória, conforme demonstrado no exemplo a seguir:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    O componente de aplicativo cliente deve definir *ppStr* como **nulo** ao chamar o método RPC.

 

 




