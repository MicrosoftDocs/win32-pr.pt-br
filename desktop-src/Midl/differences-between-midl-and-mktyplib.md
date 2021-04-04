---
title: Diferenças entre MIDL e MkTypLib
description: Diferenças entre MIDL e MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL e ODL, diferenças entre MIDL e MkTypLib
- MIDL MkTypLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006159"
---
# <a name="differences-between-midl-and-mktyplib"></a>Diferenças entre MIDL e MkTypLib

> [!Note]  
> A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.

 

Há algumas áreas-chave em que o compilador MIDL difere de MkTypLib. A maioria dessas diferenças surge porque MIDL é orientado mais em direção C-Syntax do que MkTypLib.

Em geral, você desejará usar a sintaxe MIDL em seus arquivos IDL. No entanto, se você precisar compilar um arquivo ODL existente ou manter a compatibilidade com o MkTypLib, use a opção de compilador de MIDL [**/mktyplib203**](-mktyplib203.md) para forçar o MIDL a se comportar como Mkktyplib.exe, versão 2, 3. (Esta é a última versão da ferramenta MkTypLib.) Especificamente, a opção **/mktyplib203** resolve essas diferenças:

-   sintaxe de typedef para tipos de dados complexos

    No MkTypLib, ambas as definições a seguir geram um \_ registro TKIND para "este \_ struct" na biblioteca de tipos. A marca " \_ tag struct" é opcional e, se usada, não aparecerá na biblioteca de tipos.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Se uma marca opcional estiver ausente, MIDL irá gerá-la, adicionando efetivamente uma marca à definição fornecida pelo usuário. Como a primeira definição tem uma marca, MIDL gerará um \_ registro TKIND para "This \_ struct" e um \_ alias TKIND para "This \_ struct" (definindo "This \_ struct" como um alias para " \_ tag struct"). Como a marca está ausente na segunda definição, MIDL gerará um registro TKIND \_ para um nome desconfigurado, interno ao MIDL, que não é significativo para o usuário e um alias TKIND \_ para "essa \_ struct".

    Isso tem possíveis implicações para os navegadores de biblioteca de tipos que simplesmente mostram o nome de um registro em sua interface do usuário. Se você espera que um \_ registro TKIND tenha um nome real, nomes não reconhecíveis podem aparecer na interface do usuário. Esse comportamento também se aplica às definições de [**União**](union.md) e [**Enumeração**](enum.md) , com o compilador MIDL gerando \_ uniões TKIND e \_ enumerações TKIND, respectivamente.

    MIDL também permite definições de [**struct**](struct.md), [**Union**](union.md)e [**enum**](enum.md) em estilo C. Por exemplo, a seguinte definição é válida no MIDL:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   Tipos de dados boolianos

    Em MkTypLib, o tipo de base [**booliano**](boolean.md) e o tipo de dados MkTypLib bool são equivalentes a VT \_ bool, que é mapeado para \_ booliano de Variant e que é definido como um [**curto**](short.md). No MIDL, o tipo base **booliano** é equivalente a VT \_ UI1, que é definido como um [**Char não assinado**](unsigned.md), e o tipo de dados bool é definido como um [**longo**](long.md). Isso leva a dificuldades se você misturar a sintaxe IDL e a sintaxe ODL no mesmo arquivo enquanto ainda estiver tentando manter a compatibilidade com o MkTypLib. Como os tipos de dados são tamanhos diferentes, o código de marshaling não corresponderá ao que está descrito nas informações de tipo. Se você quiser um VT \_ bool em sua biblioteca de tipos, deverá usar o \_ tipo de dados BOOL de variante.

-   Definições de GUID em arquivos de cabeçalho

    No MkTypLib, os GUIDs são definidos no arquivo de cabeçalho com uma macro que pode ser compilada condicionalmente para gerar uma predefinição de GUID ou um GUID instanciado. O MIDL normalmente coloca as predefinições de GUID em seus arquivos de cabeçalho gerados e instanciações GUID somente no arquivo gerado pelo comutador [**/IID nomedearquivo**](-iid.md) .

As seguintes diferenças no comportamento não podem ser resolvidas usando a opção [**/mktyplib203**](-mktyplib203.md) :

-   Diferenciar maiúsculas de minúsculas

    MIDL diferencia maiúsculas de minúsculas, automação OLE não é.

-   Escopo de símbolos em uma declaração de enumeração

    No MkTypLib, o escopo de símbolos em um enum é local. No MIDL, o escopo dos símbolos em uma enumeração é global, pois ele está em C. Por exemplo, o código a seguir será compilado em MkTypLib, mas irá gerar um erro de nome duplicado no MIDL:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Escopo do atributo público

    Se você aplicar o atributo [**Public**](public.md) a um bloco de interface, MkTypLib tratará cada typedef dentro desse bloco de interface como público. MIDL requer que você aplique explicitamente o atributo **Public** a esses TYPEDEFs que você deseja público.

-   Ordem de pesquisa do importlib

    Se você importar mais de uma biblioteca de tipos e se essas bibliotecas contiverem referências duplicadas, o MkTypLib resolverá isso usando a primeira referência que encontrar. MIDL usará a última referência que encontrar. Por exemplo, considerando a seguinte sintaxe ODL, a biblioteca C usará o typedef MOO da biblioteca A se você compilar com MkTypLib e o typedef MOO da biblioteca B se você compilar with MIDL:

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    A solução alternativa apropriada para isso é qualificar cada referência desse tipo com o nome da biblioteca de importação correto, desta forma:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   Tipo de dados VOID não reconhecido

    MIDL reconhece o tipo de dados [**void**](void.md) em linguagem C e não reconhece o tipo de dados void de automação OLE. Se você tiver um arquivo ODL que usa VOID, coloque essa definição na parte superior do arquivo:

    ``` syntax
#define VOID void
    ```

-   Notação exponencial

    MIDL requer que os valores expressos na notação exponencial sejam contidos entre aspas. Por exemplo, "-2,5 E + 3"

-   Valores e constantes LCID

    Normalmente, o MIDL não considera o LCID ao analisar arquivos. Para forçar esse comportamento para um valor, ou se você precisar usar notação específica de localidade ao definir uma constante, coloque o valor ou a constante entre aspas.

Para obter mais informações, consulte [**/mktyplib203**](-mktyplib203.md), [**/IID nomedearquivo**](-iid.md)e [empacotamento de tipos de dados OLE](marshaling-ole-data-types.md).

 

 




