---
title: atributo pragma
description: A diretiva \ pragma MIDL \_ Echo instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.
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

A \# diretiva **pragma MIDL \_ Echo** instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.

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

Especifica uma cadeia de caracteres que é inserida no arquivo de cabeçalho gerado. As aspas são removidas durante o processo de inserção.

</dd> <dt>

*sequência de tokens* 
</dt> <dd>

Especifica uma sequência de tokens que são inseridos no arquivo de cabeçalho gerado como parte de uma diretiva **\# pragma** sem processamento pelo compilador MIDL.

</dd> <dt>

*n* 
</dt> <dd>

Especifica o tamanho atual do pacote. Os valores válidos são 1, 2, 4, 8 e 16.

</dd> <dt>

*id* 
</dt> <dd>

Especifica o identificador de usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

As diretivas de pré-processamento c-Language que aparecem no arquivo IDL são processadas pelo pré-processador do compilador C. As diretivas de **\# definição** no arquivo IDL estão disponíveis durante a compilação de MIDL, embora não no compilador C.

Por exemplo, quando o pré-processador encontra a diretiva "definir o \# Windows 4", o pré-processador substitui todas as ocorrências de "Windows" no arquivo IDL por "4". O símbolo "WINDOWS" não está disponível em tempo de compilação C.

Para permitir que as definições de macro do pré-processador C passem pelo compilador MIDL para o compilador C, use a diretiva **\# pragma MIDL \_ Echo** ou [**cpp \_ quote**](cpp-quote.md) . Essas diretivas instruem o compilador MIDL a gerar um arquivo de cabeçalho que contém a cadeia de caracteres de parâmetro com as aspas removidas. As diretivas **\# pragma MIDL \_ Echo** e **cpp \_ quote** são equivalentes.

A diretiva **\# pragma Pack** é usada pelo compilador MIDL para controlar a embalagem de estruturas. Ele substitui a opção de linha de comando [**/ZP**](-zp.md) . A opção Pack (*n*) define o tamanho atual do pacote para um valor específico: 1, 2, 4, 8 ou 16. As opções de pacote (push) e de pacote (pop) têm as seguintes características:

-   O compilador mantém uma pilha de embalagens. Os elementos da pilha de embalagens incluem um tamanho de pacote e uma *ID* opcional. A pilha é limitada apenas pela memória disponível com o tamanho atual do pacote na parte superior da pilha.
-   O pacote (push) resulta no tamanho atual do pacote enviado para a pilha de embalagens. A pilha é limitada pela memória disponível.
-   Pack (Push,*n*) é o mesmo que Pack (push) seguido por Pack (*n*).
-   Pack (Push, *ID*) também envia por push a *ID* para a pilha de embalagens junto com o tamanho do pacote.
-   Pack (Push, *ID*, *n*) é o mesmo que Pack (Push, *ID*) seguido por Pack (*n*).
-   O pacote (pop) resulta na pop-up da pilha de embalagens. Pops desequilibrados causam avisos e definem o tamanho atual do pacote como o valor da linha de comando.
-   Se Pack (pop, *ID*, *n*) for especificado, *n* será ignorado.

O compilador MIDL coloca as cadeias de caracteres especificadas nas diretivas de [**\\ \_ aspas de CPP**](cpp-quote.md) e **pragma** no arquivo de cabeçalho na sequência em que elas são especificadas no arquivo IDL e em relação a outros componentes de interface no arquivo IDL. As cadeias de caracteres geralmente devem aparecer na seção interface-corpo do arquivo IDL após todas as operações de [**importação**](import.md) .

O compilador MIDL não tenta processar diretivas **\# pragma** que não começam com o prefixo "MIDL" \_ . Outras diretivas **\# pragma** no arquivo IDL são passadas para o arquivo de cabeçalho gerado sem alterações.

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

[**citação de CPP \_**](cpp-quote.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importe**](import.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




