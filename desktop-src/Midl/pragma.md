---
title: atributo pragma
description: A diretiva de eco midl \ pragma instrui MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no \_ arquivo de título gerado.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- atributo pragma MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ca869acddf4b0a0a098707833e889efcfccc267a3abf1949921c550cf66c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383494"
---
# <a name="pragma-attribute"></a>atributo pragma

A \# **diretiva de eco midl \_ pragma** instrui MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de título gerado.

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cadeia de caracteres* 
</dt> <dd>

Especifica uma cadeia de caracteres inserida no arquivo de header gerado. As aspas são removidas durante o processo de inserção.

</dd> <dt>

*sequência de token* 
</dt> <dd>

Especifica uma sequência de tokens que são inseridos no arquivo de título gerado como parte de uma diretiva **\# pragma** sem processamento pelo compilador MIDL.

</dd> <dt>

*n* 
</dt> <dd>

Especifica o tamanho do pacote atual. Os valores válidos são 1, 2, 4, 8 e 16.

</dd> <dt>

*id* 
</dt> <dd>

Especifica o identificador de usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

As diretivas de pré-processamento da linguagem C que aparecem no arquivo IDL são processadas pelo pré-processador do compilador C. As **\# diretivas** definem no arquivo IDL estão disponíveis durante a compilação MIDL, embora não para o compilador C.

Por exemplo, quando o pré-processador encontra a diretiva " definir WINDOWS 4", o pré-processador substitui todas as ocorrências de "WINDOWS" no arquivo \# IDL por "4". O símbolo "WINDOWS" não está disponível no tempo de compilação C.

Para permitir que as definições de macro do pré-processador C passem pelo compilador MIDL para o compilador C, use a **\# diretiva pragma midl \_ echo** ou [**cpp \_ quote.**](cpp-quote.md) Essas diretivas instruem o compilador MIDL a gerar um arquivo de header que contém a cadeia de caracteres de parâmetro com as aspas removidas. As **\# diretivas pragma midl \_ echo** e **cpp \_ quote** são equivalentes.

A **\# diretiva pragma pack** é usada pelo compilador MIDL para controlar o empacotamento de estruturas. Ele substitui a opção de linha de [**comando /Zp.**](-zp.md) A opção pack (*n*) define o tamanho do pacote atual para um valor específico: 1, 2, 4, 8 ou 16. As opções pack (push) e pack (pop) têm as seguintes características:

-   O compilador mantém uma pilha de empacotamento. Os elementos da pilha de empacotamento incluem um tamanho de pacote e uma *ID opcional*. A pilha é limitada apenas pela memória disponível com o tamanho do pacote atual na parte superior da pilha.
-   O pacote (push) resulta no tamanho do pacote atual esvasado para a pilha de empacotamento. A pilha é limitada pela memória disponível.
-   Pack (push,*n*) é o mesmo que o pacote (push) seguido por pack (*n*).
-   Pack (push, *id*) também esvaia *a ID* para a pilha de empacotamento junto com o tamanho do pacote.
-   Pack (push, *id*, *n*) é o mesmo que pack (push, *id*) seguido por pack (*n*).
-   O pacote (pop) resulta na ressão da pilha de empacotamento. Pops desbalanceados causam avisos e configuram o tamanho do pacote atual como o valor de linha de comando.
-   Se pack (pop, *id*, *n*) for especificado, *n* será ignorado.

O compilador MIDL coloca as cadeias de caracteres especificadas nas aspas [**\\ cpp \_**](cpp-quote.md) e **diretivas pragma** no arquivo de header na sequência em que são especificadas no arquivo IDL e em relação a outros componentes de interface no arquivo IDL. As cadeias de caracteres geralmente devem aparecer na seção de corpo da interface do arquivo IDL após todas as operações [**de**](import.md) importação.

O compilador MIDL não tenta processar diretivas **\# pragma** que não começam com o prefixo "midl \_ ." Outras **\# diretivas pragma** no arquivo IDL são passadas para o arquivo de header gerado sem alterações.

## <a name="examples"></a>Exemplos

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Cotação do \_ cpp**](cpp-quote.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Importação**](import.md)
</dt> <dt>

[**/zp**](-zp.md)
</dt> </dl>

 

 




