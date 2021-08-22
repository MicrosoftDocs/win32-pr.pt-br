---
title: Técnicas de IDL para melhor interface e design de método
description: Considere usar as técnicas específicas de IDL a seguir para melhorar a segurança e o desempenho ao desenvolver interfaces e métodos RPC que lidam com dados compatíveis e variantes.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3608e908742d4de4b6564787c6d8faffc29efcef81549ff50414cc7716c468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929422"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Técnicas de IDL para melhor interface e design de método

Considere usar as técnicas específicas de IDL a seguir para melhorar a segurança e o desempenho ao desenvolver interfaces e métodos RPC que lidam com dados compatíveis e variantes. Os atributos referenciados neste tópico são os atributos IDL definidos em parâmetros de método que lidam com dados compatíveis (por exemplo, o tamanho é e max é atributos) ou dados variantes \[ **\_** \] \[ **\_** \] (por exemplo, \[ **\_** \] \[  o comprimento \] é e os atributos de cadeia de caracteres).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Usando o \[ atributo range \] com parâmetros de dados compatíveis

O atributo range instrui o tempo de execução RPC a executar validação de tamanho adicional durante o \[  \] processo de desmarque de dados. Especificamente, ele verifica se o tamanho fornecido dos dados passados como o parâmetro associado está dentro do intervalo especificado.

O \[ **atributo range** \] não afeta o formato de transmissão.

Se o valor na transmissão estiver fora do intervalo permitido, o RPC lançará uma exceção RPC X INVALID BOUND ou \_ \_ \_ RPC \_ X BAD \_ \_ STUB \_ DATA. Isso fornece um nível adicional de validação de dados e pode ajudar a evitar erros comuns de segurança, como estouros de buffer. Da mesma forma, o uso do intervalo pode melhorar o desempenho do aplicativo, pois os dados compatíveis marcados com ele têm restrições claramente definidas disponíveis para consideração \[  \] pelo serviço RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Regras de gerenciamento de memória de stub do servidor RPC

É importante entender as regras de gerenciamento de memória de stub do servidor RPC ao criar os arquivos IDL para um aplicativo habilitado para RPC. Os aplicativos podem melhorar a utilização de recursos do servidor usando o intervalo em conjunto com os dados compatíveis, conforme indicado acima, bem como evitar deliberadamente a aplicação de atributos de IDL de dados de comprimento variável, como comprimento, é para dados \[  \] \[ **\_** \] compatíveis.

A aplicação de \[ **length é \_ para** \] campos de estrutura de dados definidos em um arquivo IDL não é recomendado.

## <a name="best-practices-for-variable-length-data-parameters"></a>Práticas recomendadas para parâmetros de dados de comprimento variável

A seguir estão várias práticas recomendadas a considerar ao definir os atributos IDL para estruturas de dados de tamanho variável, parâmetros de método e campos.

-   Use correlação antecipada. Geralmente, é melhor definir o parâmetro ou o campo de tamanho variável, de modo que ele ocorra imediatamente após o tipo integral de controle.

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

    em que **earlyCorr** declara o parâmetro de tamanho imediatamente antes do parâmetro de dados de comprimento variável e **lateCorr** declara o parâmetro de tamanho depois dele. O uso da correspondência antecipada melhora o desempenho geral, especialmente nos casos em que o método é chamado com frequência.

-   Para parâmetros marcados com out, size é a tupla de atributo e, em que o comprimento dos dados é conhecido no lado do cliente ou em que o cliente tem um limite superior razoável, a definição do método deve ser semelhante à seguinte em termos de atribuição de parâmetro e \[ **\_** \] sequência:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    Nesse caso, o cliente fornece um buffer de tamanho fixo para *pArr,* permitindo que o serviço RPC do lado do servidor aloce um buffer de tamanho razoável com um bom grau de garantia. Observe que, no exemplo, os dados são recebidos do servidor ( \[ **out** \] ). A definição é semelhante aos dados passados para o servidor ( \[ **em** \] ).

-   Para situações em que o componente do lado do servidor de um aplicativo RPC decide o comprimento dos dados, a definição do método deve ser semelhante à seguinte:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **RANGED \_ LONG** é um tipo definido para os stubs de cliente e de servidor e de um tamanho especificado que o cliente pode prever corretamente. No exemplo, o cliente passa *ppArr* como **NULL** e o componente de aplicativo do servidor RPC aloca a quantidade correta de memória. Após o retorno, o serviço RPC no lado do cliente aloca a memória para os dados retornados.

-   Se o cliente quiser enviar um subconjunto de uma grande matriz compatível para o servidor, o aplicativo poderá especificar o tamanho do subconjunto, conforme demonstrado no exemplo a seguir:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    Dessa forma, o RPC transmitirá *apenas elementos lLength* da matriz pela transmissão. No entanto, essa definição força o serviço RPC a alocar memória de *tamanho lSize* no lado do servidor.

-   Se o componente do aplicativo cliente determinar o tamanho máximo de uma matriz que o servidor pode retornar, mas permitir que o servidor transmita um subconjunto dessa matriz, o aplicativo poderá especificar esse comportamento definindo a IDL semelhante ao exemplo a seguir:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    O componente do aplicativo cliente especifica o tamanho máximo da matriz e o servidor especifica quantos elementos ele transmite de volta para o cliente.

-   Se o componente de aplicativo do servidor precisar retornar uma cadeia de caracteres para o componente do aplicativo cliente e se o cliente souber o tamanho máximo a ser retornado do servidor, o aplicativo poderá usar um tipo de cadeia de caracteres compatível, conforme demonstrado no exemplo a seguir:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Se o componente do aplicativo cliente não deve controlar o tamanho da cadeia de caracteres, o serviço RPC pode alocar especificamente a memória, conforme demonstrado no exemplo a seguir:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    O componente do aplicativo cliente deve definir *ppStr* como **NULL** ao chamar o método RPC.

 

 




