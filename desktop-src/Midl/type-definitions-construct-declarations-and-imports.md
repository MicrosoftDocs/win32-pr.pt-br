---
title: Definições de tipo, declarações de construção e importações
description: As definições de tipo, as declarações de construção e as importações podem ocorrer fora do corpo da interface.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- MIDL de interfaces, definições de tipo
- interfaces MIDL, declarações de construção
- MIDL de interfaces, importações
- definições de tipo MIDL
- MIDL de declarações de construção
- MIDL de importações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756911"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Definições de tipo, declarações de construção e importações

As definições de tipo, as declarações de construção e as importações podem ocorrer fora do corpo da interface. Todas as definições do arquivo IDL principal serão exibidas no arquivo de cabeçalho gerado e todos os procedimentos de todas as interfaces no arquivo IDL principal irão gerar rotinas de stub. Isso permite que os aplicativos que dão suporte a várias interfaces mesclem arquivos IDL em um único arquivo IDL combinado.

Como resultado, ele requer menos tempo para compilar os arquivos e também permite que MIDL reduza as redundâncias nos stubs gerados. Isso pode melhorar significativamente as interfaces de [**objeto**](object.md) através da capacidade de compartilhar código comum para interfaces base e interfaces derivadas. Para interfaces que não são de **objeto** , os nomes de procedimento devem ser exclusivos em todas as interfaces. Para interfaces de **objeto** , os nomes de procedimento precisam ser exclusivos somente dentro de uma interface. Observe que várias interfaces não são permitidas quando você usa a opção [**/OSF**](-osf.md)

## <a name="declarative-constructs"></a>Construções declarativas

A sintaxe para construções declarativas no arquivo IDL é semelhante àquela para C. MIDL dá suporte a todas as construções declarativas do Microsoft C/C++, exceto as seguintes:

-   Declaradores de estilo mais antigos que permitem que um Declarador seja especificado sem um especificador de tipo, como:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Declarações com inicializadores (MIDL aceita apenas declarações que estão em conformidade com a sintaxe MIDL [**const**](const.md) ).

A palavra-chave [**Import**](import.md) especifica os nomes de um ou mais arquivos IDL a serem importados. A diretiva de importação é semelhante à diretiva C [**include**](include.md) , exceto que apenas os tipos de dados são assimilados no arquivo de importação de IDL.

## <a name="constant-declaration"></a>Declaração de constante

A declaração de constante especifica as constantes [**booliana**](boolean.md), inteiro, caractere, caractere largo, Cadeia de caracteres e **void \*** . Para obter mais informações, consulte [**const**](const.md).

## <a name="general-declaration"></a>Declaração geral

Uma declaração geral é semelhante à instrução C [**typedef**](typedef.md) com a adição de atributos de tipo IDL. Exceto no modo [**/OSF**](-osf.md) , o compilador MIDL também permite uma declaração implícita na forma de uma definição de variável.

## <a name="function-declaration"></a>Declaração de função

O Declarador de função é um caso especial da declaração geral. Você pode usar atributos IDL para especificar o comportamento do tipo de retorno da função e de cada um dos parâmetros.

## <a name="examples"></a>Exemplos

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




