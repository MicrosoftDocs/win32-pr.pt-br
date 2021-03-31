---
title: Gerenciamento de memória de stub de servidor
description: Gerenciamento de memória de stub de servidor
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Gerenciamento de memória de stub de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103824034"
---
# <a name="server-stub-memory-management"></a>Gerenciamento de memória de stub de servidor

## <a name="an-introduction-to-server-stub-memory-management"></a>Uma introdução ao gerenciamento de memória Server-Stub

Os stubs gerados pelo MIDL atuam como a interface entre um processo de cliente e um processo de servidor. Um stub de cliente realiza marshaling de todos os dados passados para os parâmetros marcados com o atributo [**\[ in \]**](../midl/in.md) e os envia para o stub do servidor. O stub de servidor, após receber esses dados, reconstrói a pilha de chamadas e, em seguida, executa a função de servidor correspondente implementada pelo usuário. O stub do servidor também realiza marshaling dos dados do parâmetro marcados com o atributo [**\[ out \]**](../midl/out-idl.md) e o retorna ao aplicativo cliente.

O formato de dados com marshaling de 32 bits usado pelo MSRPC é uma versão compatível da sintaxe de transferência de data de representação (NDR) de rede. Para obter mais informações sobre esse formato, consulte [o site do grupo aberto](https://www.opengroup.org/). Para plataformas de 64 bits, uma extensão de Microsoft 64 bits para a sintaxe de transferência de NDR chamada NDR64 pode ser usada para melhorar o desempenho.

## <a name="unmarshaling-inbound-data"></a>Desempacotamento de dados de entrada

No MSRPC, o stub de cliente realiza marshaling de todos os dados de parâmetro marcados como [**\[ em \]**](../midl/in.md) um buffer contínuo para transmissão para o stub do servidor. Da mesma forma, o stub de servidor realiza marshaling de todos os dados marcados com o atributo [**\[ out \]**](../midl/out-idl.md) em um buffer contínuo para retornar ao stub do cliente. Embora a camada de protocolo de rede sob RPC possa fragmentar e armazenar o buffer para transmissão, a fragmentação é transparente para os stubs de RPC.

A alocação de memória para criar o quadro de chamada do servidor pode ser uma operação cara. O stub do servidor tentará minimizar o uso de memória desnecessário, quando possível, e supõe-se que a rotina do servidor não liberará ou Realocará dados marcados com os atributos [**\[ in \]**](../midl/in.md) ou **\[ in, out \]** . O stub de servidor tenta reutilizar os dados no buffer sempre que possível para evitar a duplicação desnecessária. A regra geral é que, se o formato de dados marshaled for igual ao formato de memória, o RPC usará ponteiros para os dados marshalled em vez de alocar memória adicional para dados formatados de forma idêntica.

Por exemplo, a chamada RPC a seguir é definida com uma estrutura cujo formato empacotado é idêntico ao seu formato na memória.

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

Nesse caso, o RPC não aloca memória adicional para os dados referenciados por *plInStructure*; em vez disso, ele simplesmente passa o ponteiro para os dados empacotados para a implementação da função do lado do servidor. O stub do servidor RPC verifica o buffer durante o processo de desempacotamento se o stub for compilado usando o sinalizador "-robusto" (que é uma configuração padrão na versão recente do nmost do compilador MIDL). O RPC garante que os dados passados para a implementação da função do lado do servidor sejam válidos.

Lembre-se de que a memória é alocada para *plOutStructure*, já que nenhum dado é passado para o servidor para ele.

## <a name="memory-allocation-for-inbound-data"></a>Alocação de memória para dados de entrada

Podem surgir casos em que o stub do servidor aloca memória para dados de parâmetro marcados com os atributos [**\[ in \]**](../midl/in.md) ou **\[ in \] , out** . Isso ocorre quando o formato de dados empacotados difere do formato de memória ou quando as estruturas que compõem os dados de marshaling são suficientes e devem ser lidas atomicamente pelo stub do servidor RPC. A lista abaixo mostra vários casos comuns em que a memória deve ser alocada para os dados recebidos pelo stub do servidor.

-   Os dados são uma matriz variável ou uma matriz de variação em conformidade. Essas são as matrizes (ou ponteiros para matrizes) que têm o [**\[ comprimento \_ () \]**](../midl/length-is.md) ou o [**\[ primeiro atributo \_ é () \]**](../midl/first-is.md) definido nelas. No NDR, somente o primeiro elemento dessas matrizes é empacotado e transmitido. Por exemplo, no trecho de código abaixo, os dados passados no parâmetro *VP* terão memória alocada para ele.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   Os dados são uma cadeia de caracteres de tamanho ou uma cadeia de caracteres não compatível. Essas cadeias de caracteres geralmente são ponteiros para dados de caractere marcados com o atributo [**\[ Size \_ is () \]**](../midl/size-is.md) . No exemplo a seguir, a cadeia de caracteres passada para a função **dimensionada** do lado do servidor terá memória alocada, enquanto a cadeia de caracteres passada para a função **normalstring** será reutilizada.

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

-   Os dados são um tipo simples cujo tamanho da memória difere de seu tamanho de marshaling, como **enum16** e **\_ \_ int3264**.
-   Os dados são definidos por uma estrutura cujo alinhamento de memória é menor do que o alinhamento natural, contém qualquer um dos tipos de dados acima ou tem um preenchimento de byte à direita. Por exemplo, a estrutura de dados complexa a seguir forçou o alinhamento de 2 bytes e tem preenchimento no final.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   Os dados contêm uma estrutura que deve ser empacotada em campo por campo. Esses campos incluem ponteiros de interface definidos em interfaces DCOM; ponteiros ignorados; valores inteiros definidos com o [**\[ atributo \] Range**](../midl/range.md) ; os elementos de matrizes definidos com a [**\[ conexão \_ Marshal \]**](../midl/wire-marshal.md), [**\[ user \_ Marshal \]**](../midl/user-marshal.md), [**\[ Transmit \_ como \]**](../midl/transmit-as.md) e [**\[ representam \_ como \]**](../midl/represent-as.md) atributos e estruturas de dados complexas inseridas.
-   Os dados contêm uma União, uma estrutura que contém uma União ou uma matriz de uniões. Somente a ramificação específica da União é empacotada na conexão.
-   Os dados contêm uma estrutura com uma matriz de conformidade multidimensional que tem pelo menos uma dimensão não fixa.
-   Os dados contêm uma matriz de estruturas complexas.
-   Os dados contêm uma matriz de tipos de dados simples, como **enum16** e **\_ \_ int3264**.
-   Os dados contêm uma matriz de ponteiros de referência e de interface.
-   Os dados têm um atributo [**\[ Force \_ ALLOCATE \]**](../midl/force-allocate.md) aplicado a um ponteiro.
-   Os dados têm um atributo [**\[ ALLOCATE (todos os \_ nós) \]**](../midl/allocate.md) aplicado a um ponteiro.
-   Os dados têm um atributo de [**\[ \_ contagem \] de bytes**](../midl/byte-count.md) aplicado a um ponteiro.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>Dados de 64 bits e a sintaxe de transferência NDR64

Conforme mencionado anteriormente, os dados de 64 bits são marshalled usando uma sintaxe de transferência de 64 bits específica chamada NDR64. Essa sintaxe de transferência foi desenvolvida para resolver o problema específico que surge quando os ponteiros são empacotados no NDR de 32 bits e transmitidos para um stub de servidor em uma plataforma de 64 bits. Nesse caso, um ponteiro de dados de 32 bits com marshaling não corresponde a um de 64 bits, e a alocação de memória invariavelmente ocorrerá. Para criar um comportamento mais consistente em plataformas de 64 bits, a Microsoft desenvolveu uma nova sintaxe de transferência chamada NDR64.

Um exemplo que ilustra esse problema é o seguinte:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Essa estrutura, quando empacotada, será reutilizada pelo stub do servidor em um sistema de 32 bits. No entanto, se o stub do servidor residir em um sistema de 64 bits, os dados empacotados por NDR terão 4 bytes de comprimento, mas o tamanho de memória necessário será 8. Como resultado, a alocação de memória é forçada e a reutilização de buffer raramente ocorrerá. NDR64 resolve esse problema fazendo o tamanho do marshaling de um ponteiro de 64 bits.

Em contraste com o NDR de 32 bits, tyes de dados simples como **enum16** e **\_ \_ int3264** não tornam uma estrutura ou matriz complexa em NDR64. Da mesma forma, os valores de preenchimento à direita não tornam uma estrutura complexa. Ponteiros de interface são tratados como ponteiros exclusivos no nível superior; Como resultado, estruturas e matrizes contendo ponteiros de interface não são consideradas complexas e não exigem alocação de memória específica para seu uso.

## <a name="initializing-outbound-data"></a>Inicializando dados de saída

Depois que todos os dados de entrada tiverem sido desempacotados, o stub do servidor precisará inicializar os ponteiros somente de saída marcados com o atributo [**\[ out \]**](../midl/out-idl.md) .


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



Na chamada acima, o stub do servidor deve inicializar *plOutStructure* porque ele não estava presente nos dados empacotados e é um ponteiro de [**\[ referência \]**](../midl/ref.md) implícito que deve ser disponibilizado para a implementação da função de servidor. O stub do servidor RPC Inicializa e zera quaisquer ponteiros somente de referência de nível superior com o atributo [**\[ out \]**](../midl/out-idl.md) . Quaisquer ponteiros de referência **\[ out \]** abaixo dele são inicializados recursivamente também. A recursão é interrompida a qualquer ponteiro com os atributos [**\[ Unique \]**](../midl/unique.md) ou [**\[ PTR \]**](../midl/ptr.md) definidos neles.

A implementação da função de servidor não pode alterar diretamente valores de ponteiro de nível superior e, portanto, não pode realocá-los. Por exemplo, na implementação de **ProcessRpcStructure** acima, o código a seguir é inválido:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure* é um valor de pilha e sua alteração não é propagada de volta para RPC. A implementação da função de servidor pode tentar evitar a alocação ao tentar liberar *plOutStructure*, o que pode resultar em corrupção de memória. O stub de servidor alocará espaço para o ponteiro de nível superior na memória (no caso de ponteiro para ponteiro) e uma estrutura simples de nível superior cujo tamanho na pilha é menor do que o esperado.

O cliente pode, em determinadas circunstâncias, especificar o tamanho de alocação de memória do lado do servidor. No exemplo a seguir, o cliente especifica o tamanho dos dados de saída no parâmetro de *tamanho* de entrada.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Depois de desempacotar os dados de entrada, incluindo o *tamanho*, o stub do servidor aloca um buffer para *VP* com um tamanho de "tamanho (caractere) \* ". Depois que o espaço tiver sido alocado, o stub do servidor zerará o buffer. Observe que nesse caso específico, o stub aloca a memória com o usuário de **MIDL \_ \_ ALLOCATE ()**, já que o tamanho do buffer é determinado em tempo de execução.

Lembre-se de que, no caso das interfaces DCOM, os stubs gerados por MIDL podem não estar envolvidos se o cliente e o servidor compartilharem o mesmo apartamento COM ou se **ICallFrame** for implementado. Nesse caso, o servidor não pode depender do comportamento de alocação e precisa verificar a memória no tamanho do cliente de forma independente.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implementações de função do lado do servidor e marshaling de dados de saída

Logo após o desempacotamento em dados de entrada e a inicialização da memória alocada para conter dados de saída, o stub do servidor RPC executa a implementação do lado do servidor da função chamada pelo cliente. Neste momento, o servidor pode modificar os dados marcados especificamente com o atributo **\[ in, out \]** e ele pode preencher a memória alocada para dados somente de saída (os dados marcados com [**\[ out \]**](../midl/out-idl.md)).

As regras gerais para a manipulação de dados de parâmetro marshalled são simples: o servidor só pode alocar uma nova memória ou modificar a memória especificamente alocada pelo stub do servidor. A realocação ou liberação de memória existente para dados pode ter um impacto negativo nos resultados e no desempenho da chamada de função, e pode ser muito difícil de depurar.

Logicamente, o servidor RPC reside em um espaço de endereço diferente do cliente e, em geral, pode ser considerado que eles não compartilham memória. Como resultado, é seguro que a implementação da função de servidor use os dados marcados com o atributo [**\[ in \]**](../midl/in.md) como a memória "Scratch" sem afetar os endereços de memória do cliente. Dito isso, o servidor não deve tentar realocar **\[ \] ou liberar dados** , deixando o controle desses espaços para o próprio stub do servidor RPC.

Em geral, a implementação da função de servidor não precisa realocar ou liberar dados marcados com o atributo **\[ in, out \]** . Para dados de tamanho fixo, a lógica de implementação de função pode modificar os dados diretamente. Da mesma forma, para dados de tamanho variável, a implementação da função não deve modificar o valor do campo fornecido para o atributo [**\[ Size \_ () \]**](../midl/size-is.md) , seja. Altere o valor do campo usado para dimensionar os resultados de dados em um buffer menor ou maior retornado ao cliente que pode estar mal equipado para lidar com o comprimento anormal.

Se ocorrerem circunstâncias em que a rotina do servidor precisa realocar a memória usada pelos dados marcados com o atributo **\[ in, out \]** , é totalmente possível que a implementação da função do lado do servidor não saiba se o ponteiro fornecido pelo stub é a memória alocada com o **usuário de MIDL \_ \_ ALLOCATE ()** ou o buffer de fios com marshaling realizado. Para contornar esse problema, o MS RPC pode garantir que nenhum vazamento de memória ou corrupção ocorra se o atributo [**\[ Force \_ ALLOCATE \]**](../midl/force-allocate.md) estiver definido nos dados. Quando **\[ forçar \_ alocação \]** for definido, o stub do servidor sempre alocará memória para o ponteiro, embora a limitação seja a redução do desempenho para cada uso.

Quando a chamada retorna da implementação da função do lado do servidor, o stub do servidor realiza marshaling dos dados marcados com o atributo [**\[ out \]**](../midl/out-idl.md) e os envia para o cliente. Lembre-se de que o stub não empacota os dados se a implementação da função do lado do servidor lançar uma exceção.

## <a name="releasing-allocated-memory"></a>Liberando memória alocada

O stub do servidor RPC liberará a memória da pilha depois que a chamada for retornada da função do lado do servidor, se ocorrer uma exceção ou não. O stub do servidor libera toda a memória alocada pelo stub, bem como qualquer memória alocada com o **usuário de MIDL \_ \_ ALLOCATE ()**. A implementação da função do lado do servidor sempre deve fornecer um estado consistente de RPC, emitindo uma exceção ou retornando um código de erro. Se a função falhar durante a população de estruturas de dados complicadas, ela deverá garantir que todos os ponteiros apontem para dados válidos ou sejam definidos como **NULL**.

Durante esse passo, o stub do servidor libera toda a memória que não faz parte do buffer de marshaling que contém os dados [**\[ em \]**](../midl/in.md) . Uma exceção a esse comportamento são os dados com o atributo [**\[ ALLOCATE (não \_ livre) \]**](../midl/allocate.md) definido neles-o stub do servidor não libera nenhuma memória associada a esses ponteiros.

Depois que o stub do servidor liberar a memória alocada pelo stub e a implementação da função, o stub chamará uma função de notificação específica se o atributo [**\[ notificar do \_ sinalizador \]**](../midl/notify-flag.md) for especificado para dados específicos.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshaling de uma lista vinculada por RPC – um exemplo


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



No exemplo acima, o formato de memória para **LinkedList** será idêntico ao formato de conexão com marshaling. Como resultado, o stub do servidor não aloca memória para toda a cadeia de ponteiros de dados no *pIn*. Em vez disso, o RPC reutiliza o buffer de conexão para toda a lista vinculada. Da mesma forma, o stub não aloca memória para *pinagem*, mas, em vez disso, reutiliza o buffer de conexão realizado pelo cliente.

Como a assinatura de função contém um parâmetro de saída, *pout*, o stub do servidor aloca memória para conter os dados retornados. A memória alocada inicialmente é zerada, com **pNext** definido como **NULL**. O aplicativo pode alocar a memória para uma nova lista vinculada e apontar *pout* -> **pNext** para ela. o *pIn* e a lista vinculada que ele contém podem ser usados como uma área de rascunho, mas o aplicativo não deve alterar nenhum dos ponteiros pNext.

O aplicativo pode alterar livremente o conteúdo da lista vinculada apontada por *pinagem*, mas não deve alterar nenhum dos ponteiros do **pNext** , permitindo apenas o link de nível superior em si. Se o aplicativo decidir encurtar a lista vinculada, não poderá saber se um determinado ponteiro **pNext** vincula para um buffer interno de RPC ou um buffer especificamente alocado com o **\_ usuário MIDL \_ ALLOCATE ()**. Para contornar esse problema, você adiciona uma declaração de tipo específica para ponteiros de lista vinculada que força a alocação do usuário, como visto no código abaixo.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Esse atributo força o stub do servidor a alocar cada nó da lista vinculada separadamente e o aplicativo pode liberar a parte reduzida da lista vinculada chamando o **\_ usuário MIDL \_ Free ()**. Em seguida, o aplicativo pode definir com segurança o ponteiro **pNext** no final da lista vinculada recentemente encurtada para **NULL**.

 

 