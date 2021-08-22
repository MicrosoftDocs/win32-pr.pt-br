---
title: Gerenciamento de memória de stub do servidor
description: Gerenciamento de memória de stub do servidor
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Gerenciamento de memória de stub do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c772678e28a51c4d5162472bc7b0ef73e19888feefbd0e1890cb13f65650425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925183"
---
# <a name="server-stub-memory-management"></a>Gerenciamento de memória de stub do servidor

## <a name="an-introduction-to-server-stub-memory-management"></a>Uma introdução ao gerenciamento Server-Stub memória

Stubs gerados por MIDL atuam como a interface entre um processo de cliente e um processo de servidor. Um stub de cliente faz marshal de todos os dados passados para parâmetros marcados com o atributo [**\[ in \]**](../midl/in.md) e os envia para o stub do servidor. O stub do servidor, ao receber esses dados, reconstrói a pilha de chamada e, em seguida, executa a função de servidor implementada pelo usuário correspondente. O stub do servidor também faz marshal dos dados de parâmetro marcados com o atributo [**\[ out \]**](../midl/out-idl.md) e os retorna para o aplicativo cliente.

O formato de dados com marshal de 32 bits usado pelo MSRPC é uma versão em conformidade da sintaxe de transferência de NDR (Representação de Dados de Rede). Para obter mais informações sobre esse formato, consulte [The Open Group website](https://www.opengroup.org/). Para plataformas de 64 bits, uma extensão de 64 bits da Microsoft para a sintaxe de transferência NDR chamada NDR64 pode ser usada para melhorar o desempenho.

## <a name="unmarshaling-inbound-data"></a>Desmarcar dados de entrada

No MSRPC, o stub do cliente empacota [**\[ \]**](../midl/in.md) todos os dados de parâmetro marcados como em um buffer contínuo para transmissão para o stub do servidor. Da mesma forma, o stub do servidor empacota todos os dados marcados com o atributo [**\[ out \]**](../midl/out-idl.md) em um buffer contínuo para retornar ao stub do cliente. Embora a camada de protocolo de rede abaixo do RPC possa fragmentar e em pacotes o buffer para transmissão, a fragmentação é transparente para os stubs RPC.

A alocação de memória para criar o quadro de chamada do servidor pode ser uma operação cara. O stub do servidor tentará minimizar o uso desnecessário de memória quando possível e supõe-se que [**\[ \]**](../midl/in.md) a rotina do servidor não liberará ou relocará **\[ \]** os dados marcados com os atributos de entrada ou entrada e saída. O stub do servidor tenta reutilizar dados no buffer sempre que possível para evitar duplicação desnecessária. A regra geral é que, se o formato de dados com marshaling for o mesmo que o formato de memória, o RPC usará ponteiros para os dados marshallados em vez de alocar memória adicional para dados formatados de forma idêntica.

Por exemplo, a chamada RPC a seguir é definida com uma estrutura cujo formato marshaled é idêntico ao formato na memória.

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

Nesse caso, o RPC não aloca memória adicional para os dados referenciados por *plInStructure*; em vez disso, ele simplesmente passa o ponteiro para os dados empacotados para a implementação da função do lado do servidor. O stub do servidor RPC verifica o buffer durante o processo de desmarque se o stub é compilado usando o sinalizador "-robust" (que é uma configuração padrão na versão mais recente do compilador MIDL). O RPC garante que os dados passados para a implementação da função do lado do servidor são válidos.

Esteja ciente de que a memória é alocada para *plOutStructure,* pois nenhum dado é passado para o servidor para ele.

## <a name="memory-allocation-for-inbound-data"></a>Alocação de memória para dados de entrada

Podem surgir casos em que o stub do servidor aloca memória para dados de parâmetro marcados com os atributos [**\[ in \]**](../midl/in.md) **\[ ou in, \] out.** Isso ocorre quando o formato de dados marshaled difere do formato de memória ou quando as estruturas que compõem os dados marshaled são complexas suficientes e devem ser lidas atomicamente pelo stub do servidor RPC. Veja abaixo vários casos comuns em que a memória deve ser alocada para os dados recebidos pelo stub do servidor.

-   Os dados são uma matriz variável ou uma matriz variável compatível. Essas são matrizes (ou ponteiros para matrizes) que têm o comprimento [**\[ \_ is() \]**](../midl/length-is.md) ou o primeiro atributo [**\[ \_ is() \]**](../midl/first-is.md) definido neles. Na NDR, somente o primeiro elemento dessas matrizes é marshalado e transmitido. Por exemplo, no snippet de código abaixo, os dados passados no *parâmetro pv* terão memória alocada para ele.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   Os dados são uma cadeia de caracteres dimensionada ou não compatível. Essas cadeias de caracteres geralmente são ponteiros para dados de caractere marcados com [**\[ o atributo \_ \] size is().**](../midl/size-is.md) No exemplo abaixo, a cadeia de caracteres passada para a função do lado do servidor **SizedString** terá memória alocada, enquanto a cadeia de caracteres passada para a **função NormalString** será reutilizada.

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   Os dados são um tipo simples cujo tamanho de memória é diferente do tamanho de marshaled, como **enum16** e **\_ \_ int3264.**
-   Os dados são definidos por uma estrutura cujo alinhamento de memória é menor que o alinhamento natural, contém qualquer um dos tipos de dados acima ou tem preenchimento de byte à parte inferior. Por exemplo, a estrutura de dados complexa a seguir força o alinhamento de 2 byte e tem preenchimento no final.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   Os dados contêm uma estrutura que deve ser marshalada campo por campo. Esses campos incluem ponteiros de interface definidos em interfaces DCOM; ponteiros ignorados; valores inteiros definidos com o atributo [**\[ range; \]**](../midl/range.md) elementos de matrizes definidos com o marshal de transmissão [**\[ \_ \]**](../midl/transmit-as.md) [**\[ \_ \] ,**](../midl/wire-marshal.md) [**\[ \_ \]**](../midl/represent-as.md) [**\[ \_ \]**](../midl/user-marshal.md)marshal de usuário , transmitem como e representam como atributos; e estruturas de dados complexas inseridas.
-   Os dados contêm uma união, uma estrutura que contém uma união ou uma matriz de uniões. Somente o branch específico da união é marshalado na transmissão.
-   Os dados contêm uma estrutura com uma matriz compatível multidimensional que tem pelo menos uma dimensão não fixa.
-   Os dados contêm uma matriz de estruturas complexas.
-   Os dados contêm uma matriz de tipos de dados simples, **como enum16** e **\_ \_ int3264.**
-   Os dados contêm uma matriz de ponteiros ref e interface.
-   Os dados têm um [**\[ atributo force \_ allocate \]**](../midl/force-allocate.md) aplicado a um ponteiro.
-   Os dados têm um [**\[ atributo allocate(all \_ nodes) \]**](../midl/allocate.md) aplicado a um ponteiro.
-   Os dados têm um [**\[ atributo de contagem \_ de \] byte**](../midl/byte-count.md) aplicado a um ponteiro.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>Dados de 64 bits e sintaxe de transferência NDR64

Conforme mencionado anteriormente, os dados de 64 bits são marshallados usando uma sintaxe específica de transferência de 64 bits chamada NDR64. Essa sintaxe de transferência foi desenvolvida para resolver o problema específico que surge quando os ponteiros são marshalados em NDR de 32 bits e transmitidos para um stub de servidor em uma plataforma de 64 bits. Nesse caso, um ponteiro de dados de 32 bits marshaled não corresponderá a um de 64 bits e a alocação de memória ocorrerá invariavelmente. Para criar um comportamento mais consistente em plataformas de 64 bits, a Microsoft desenvolveu uma nova sintaxe de transferência chamada NDR64.

Um exemplo que ilustra esse problema é o seguinte:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Essa estrutura, quando marshaled, será reutilizada pelo stub do servidor em um sistema de 32 bits. No entanto, se o stub do servidor residir em um sistema de 64 bits, os dados com marshal de NDR terão 4 bytes de comprimento, mas o tamanho de memória necessário será 8. Como resultado, a alocação de memória é forçada e a reutilização de buffer raramente ocorrerá. NDR64 resolve esse problema tornando o tamanho marshaled de um ponteiro de 64 bits.

Ao contrário da NDR de 32 bits, os tyes de dados simples, como **enum16** e **\_ \_ int3264,** não fazem uma estrutura ou matriz complexa em NDR64. Da mesma forma, os valores de painel à direita não torna uma estrutura complexa. Ponteiros de interface são tratados como ponteiros exclusivos no nível superior; Como resultado, as estruturas e matrizes que contêm ponteiros de interface não são consideradas complexas e não exigirão alocação de memória específica para seu uso.

## <a name="initializing-outbound-data"></a>Inicializando dados de saída

Depois que todos os dados de entrada foram desmarcados, o stub do servidor precisa inicializar os ponteiros somente de saída marcados com o [**\[ atributo out. \]**](../midl/out-idl.md)


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



Na chamada acima, o stub do servidor deve inicializar *plOutStructure* porque ele não estava presente nos dados empacotados e é um ponteiro [**\[ ref \]**](../midl/ref.md) implícito que deve ser disponibilizado para a implementação da função de servidor. O stub do servidor RPC inicializa e zera todos os ponteiros somente referência de nível superior com o [**\[ atributo out. \]**](../midl/out-idl.md) Todos **\[ os ponteiros \]** de referência de saída abaixo dele também são inicializados recursivamente. A recursão para em qualquer ponteiro com os [**\[ atributos exclusivos \]**](../midl/unique.md) ou [**\[ ptr \]**](../midl/ptr.md) definidos neles.

A implementação da função de servidor não pode alterar diretamente os valores de ponteiro de nível superior e, portanto, não pode realocar esses valores. Por exemplo, na implementação de **ProcessRpcStructure** acima, o código a seguir é inválido:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure é* um valor de pilha e sua alteração não é propagada de volta para RPC. A implementação da função de servidor pode tentar evitar a alocação ao tentar liberar *plOutStructure*, o que pode resultar em corrupção de memória. O stub do servidor alocará espaço para o ponteiro de nível superior na memória (no caso de ponteiro para ponteiro) e uma estrutura simples de nível superior cujo tamanho na pilha é menor do que o esperado.

O cliente pode, em determinadas circunstâncias, especificar o tamanho da alocação de memória do lado do servidor. No exemplo a seguir, o cliente especifica o tamanho dos dados de saída no parâmetro de *tamanho de* entrada.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Depois de desmarcar os dados de entrada, incluindo *size*, o stub do servidor aloca um buffer para *pv* com um tamanho de "tamanho de sizeof(char)". \* Depois que o espaço tiver sido alocado, o stub do servidor zera o buffer. Observe que, nesse caso específico, o stub aloca a memória com **MIDL \_ user \_ allocate()**, uma vez que o tamanho do buffer é determinado em runtime.

Esteja ciente de que, no caso de interfaces DCOM, os stubs gerados por MIDL poderão não estar envolvidos se o cliente e o servidor compartilharem o mesmo apartment COM ou se **ICallFrame** for implementado. Nesse caso, o servidor não pode depender do comportamento de alocação e precisa verificar de forma independente a memória do tamanho do cliente.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implementações de função do lado do servidor e marshaling de dados de saída

Imediatamente após a unmarshalling em dados de entrada e a inicialização da memória alocada para conter dados de saída, o stub do servidor RPC executa a implementação do lado do servidor da função chamada pelo cliente. Neste momento, o servidor pode modificar os dados especificamente marcados com o atributo **\[ in, out \]** e pode preencher a memória alocada para dados somente de saída (os [**\[ \]**](../midl/out-idl.md)dados marcados com saída ).

As regras gerais para a manipulação de dados de parâmetro marshalled são simples: o servidor só pode alocar nova memória ou modificar a memória alocada especificamente pelo stub do servidor. Realocar ou liberar memória existente para dados pode ter um impacto negativo nos resultados e no desempenho da chamada de função e pode ser muito difícil de depurar.

Logicamente, o servidor RPC reside em um espaço de endereço diferente do cliente e geralmente pode ser considerado que eles não compartilham memória. Como resultado, é seguro [**\[ \]**](../midl/in.md) para a implementação da função de servidor usar os dados marcados com o no atributo como memória "rascunho" sem afetar os endereços de memória do cliente. Dito isso, o servidor não deve tentar **\[ \]** relocar ou liberar dados, deixando o controle desses espaços para o próprio stub do servidor RPC.

Em geral, a implementação da função de servidor não precisa relocar ou liberar dados marcados com o **\[ atributo in, out. \]** Para dados de tamanho fixo, a lógica de implementação de função pode modificar diretamente os dados. Da mesma forma, para dados de tamanho variável, a implementação da função também não deve modificar o valor do campo fornecido para o atributo [**\[ \_ \] size is().**](../midl/size-is.md) Alterar o valor do campo usado para tamanho dos dados resulta em um buffer menor ou maior retornado ao cliente, que pode estar mal equipado para lidar com o tamanho anormal.

Se ocorrerem circunstâncias em que a rotina do servidor precisa relocar a memória usada pelos dados marcados com o atributo **\[ in, out, \]** é totalmente possível que a implementação da função do lado do servidor não saiba se o ponteiro fornecido pelo stub é para a memória alocada com o usuário MIDL allocate() ou o buffer de transmissão **\_ \_ marshaled.** Para resolver esse problema, o MS RPC pode garantir que nenhuma perda de memória ou corrupção ocorra se o atributo [**\[ force \_ \] allocate**](../midl/force-allocate.md) estiver definido nos dados. Quando **\[ force \_ \] allocate** estiver definido, o stub do servidor sempre alocará memória para o ponteiro, embora a advertência seja que o desempenho diminuirá para cada uso dele.

Quando a chamada retorna da implementação da função do lado do servidor, o stub do servidor faz marshal dos dados marcados com o atributo [**\[ out \]**](../midl/out-idl.md) e os envia para o cliente. Esteja ciente de que o stub não faz marshal dos dados se a implementação da função do lado do servidor lançar uma exceção.

## <a name="releasing-allocated-memory"></a>Liberando memória alocada

O stub do servidor RPC liberará a memória da pilha depois que a chamada tiver retornado da função do lado do servidor, independentemente de uma exceção ocorrer ou não. O stub do servidor libera toda a memória alocada pelo stub, bem como qualquer memória alocada com **o usuário MIDL \_ \_ allocate()**. A implementação da função do lado do servidor sempre deve dar ao RPC um estado consistente, lançando uma exceção ou retornando um código de erro. Se a função falhar durante a população de estruturas de dados complicadas, ela deverá garantir que todos os ponteiros apontem para dados válidos ou sejam definidos como **NULL.**

Durante essa passagem, o stub do servidor libera toda a memória que não faz parte do buffer com marshaling que contém [**\[ o nos \]**](../midl/in.md) dados. Uma exceção a esse comportamento são os dados com o atributo [**\[ allocate(don't \_ free) \]**](../midl/allocate.md) definido neles – o stub do servidor não libera nenhuma memória associada a esses ponteiros.

Depois que o stub do servidor liberar a memória alocada pelo stub e pela implementação da função, o stub chamará uma função de notificação específica se o atributo [**\[ de \_ \]**](../midl/notify-flag.md) sinalizador de notificação for especificado para dados específicos.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshalling a Linked List over RPC – um exemplo


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



No exemplo acima, o formato de memória para **LINKEDLIST** será idêntico ao formato de transmissão marshaled. Como resultado, o stub do servidor não aloca memória para toda a cadeia de ponteiros de dados em *pIn*. Em vez disso, o RPC reutiliza o buffer de transmissão para toda a lista vinculada. Da mesma forma, o stub não aloca memória para *pInOut,* mas, em vez disso, reutiliza o buffer de transmissão marshaled pelo cliente.

Como a assinatura da função contém um parâmetro de saída, *pOut*, o stub do servidor aloca memória para conter os dados retornados. A memória alocada inicialmente é zerada, com **pNext definido** como **NULL.** O aplicativo pode alocar a memória para uma nova lista vinculada e apontar  -> **pOut pNext** a ela. *pIn* e a lista vinculada que ele contém podem ser usados como uma área de rascunho, mas o aplicativo não deve alterar nenhum dos ponteiros pNext.

O aplicativo pode alterar livremente o conteúdo da lista vinculada apontada por *pInOut,* mas não deve alterar nenhum dos ponteiros **pNext,** muito menos o próprio link de nível superior. Se o aplicativo decidir reduzir a lista vinculada, ele não poderá saber se qualquer ponteiro **pNext** específico vincula t a um buffer interno RPC ou a um buffer alocado especificamente com **o usuário MIDL \_ \_ allocate().** Para resolver esse problema, você adiciona uma declaração de tipo específica para ponteiros de lista vinculada que força a alocação do usuário, conforme visto no código abaixo.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Esse atributo força o stub do servidor a alocar cada nó da lista vinculada separadamente, e o aplicativo pode liberar a parte abreviada da lista vinculada chamando o usuário **MIDL \_ \_ free()**. O aplicativo pode definir com segurança o **ponteiro pNext** no final da lista vinculada abreviada recentemente como **NULL.**

 

 