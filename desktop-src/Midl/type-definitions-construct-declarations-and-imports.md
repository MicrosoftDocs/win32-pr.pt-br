---
title: Definições de tipo, declarações de constructo e importações
description: Definições de tipo, declarações de constructo e importações podem ocorrer fora do corpo da interface.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfaces MIDL, definições de tipo
- interfaces MIDL, declarações de constructo
- interfaces MIDL, importações
- definições de tipo MIDL
- declarações de constructo MIDL
- importa MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1f80bca0a5d03ea0e935b05f973a6370c4180c9ce5c0fe7dea5d8f5c9c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829216"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Definições de tipo, declarações de constructo e importações

Definições de tipo, declarações de constructo e importações podem ocorrer fora do corpo da interface. Todas as definições do arquivo IDL principal serão exibidas no arquivo de header gerado e todos os procedimentos de todas as interfaces no arquivo IDL principal gerarão rotinas de stub. Isso permite que aplicativos que suportam várias interfaces mesmem arquivos IDL em um único arquivo IDL combinado.

Como resultado, ele requer menos tempo para compilar os arquivos e também permite que MIDL reduza redundâncias nos stubs gerados. Isso pode melhorar significativamente [**as**](object.md) interfaces de objeto por meio da capacidade de compartilhar código comum para interfaces base e interfaces derivadas. Para interfaces **que não** são de objeto, os nomes de procedimento devem ser exclusivos em todas as interfaces. Para **interfaces** de objeto, os nomes de procedimento precisam ser exclusivos somente em uma interface. Observe que várias interfaces não são permitidas quando você usa a [**opção /osf.**](-osf.md)

## <a name="declarative-constructs"></a>Constructos declarativos

A sintaxe para construções declarativas no arquivo IDL é semelhante à do C. MIDL dá suporte a todos os constructos declarativos do Microsoft C/C++, exceto o seguinte:

-   Declaradores de estilo mais antigos que permitem que um declarador seja especificado sem um especificador de tipo, como:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Declarações com inicializadores (MIDL aceita apenas declarações que estão em conformidade com a sintaxe midl [**const).**](const.md)

A [**palavra-chave**](import.md) import especifica os nomes de um ou mais arquivos IDL a importar. A diretiva de importação é semelhante à diretiva [**de**](include.md) inclusão C, exceto pelo fato de que apenas os tipos de dados são desalocados no arquivo IDL de importação.

## <a name="constant-declaration"></a>Declaração constante

A declaração de constante especifica constantes [**boolianas,**](boolean.md)inteiros, caracteres, caractere largo, cadeia de caracteres e **void \** _ constantes. Para obter mais informações, consulte [_ *const* *](const.md).

## <a name="general-declaration"></a>Declaração geral

Uma declaração geral é semelhante à instrução [**typedef**](typedef.md) C com a adição de atributos de tipo IDL. Exceto no [**modo /osf,**](-osf.md) o compilador MIDL também permite uma declaração implícita na forma de uma definição de variável.

## <a name="function-declaration"></a>Declaração de função

O declarador de função é um caso especial da declaração geral. Você pode usar atributos IDL para especificar o comportamento do tipo de retorno de função e cada um dos parâmetros.

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

 

 




