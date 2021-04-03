---
title: Atributo cpp_quote
description: A \_ palavra-chave quote quot instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote do atributo MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006666"
---
# <a name="cpp_quote-attribute"></a>\_atributo de citação cpp

A palavra-chave **\_ quote quot** instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cadeia de caracteres* 
</dt> <dd>

Especifica uma cadeia de caracteres entre aspas emitida no arquivo de cabeçalho gerado. A cadeia de caracteres deve estar entre aspas para evitar a expansão pelo pré-processador de C.

</dd> </dl>

## <a name="remarks"></a>Comentários

As diretivas de pré-processamento c-Language que aparecem no arquivo IDL são processadas pelo pré-processador do compilador C. As diretivas de **\# definição** no arquivo IDL estão disponíveis durante a compilação de MIDL, mas não estão disponíveis para o compilador C.

Por exemplo, quando o pré-processador encontra a diretiva "definir o \# Windows 4", o pré-processador substitui todas as ocorrências de "Windows" no arquivo IDL por "4". O símbolo "WINDOWS" não está disponível durante a compilação em linguagem C.

Para permitir que as definições de macro do pré-processador C passem pelo compilador MIDL para o compilador C, use a diretiva **\# pragma MIDL \_ Echo** ou **cpp \_ quote** . Essas diretivas instruem o compilador MIDL a gerar um arquivo de cabeçalho que contém a cadeia de caracteres de parâmetro com as aspas removidas. As diretivas **\# pragma MIDL \_ Echo** e **cpp \_ quote** são equivalentes.

O compilador MIDL coloca as cadeias de caracteres especificadas nas diretivas de **\_ aspas de CPP** e [**pragma**](pragma.md) no arquivo de cabeçalho na sequência em que elas são especificadas no arquivo IDL e em relação a outros componentes de interface no arquivo IDL. As cadeias de caracteres normalmente devem aparecer na seção corpo de interface de arquivo IDL após todas as operações de [**importação**](import.md) .

## <a name="examples"></a>Exemplos

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importe**](import.md)
</dt> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




