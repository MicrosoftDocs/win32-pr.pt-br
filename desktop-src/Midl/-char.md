---
title: comutador/Char
description: A opção/Char ajuda a garantir que o compilador de MIDL e o compilador C operem juntos corretamente para todos os tipos char e Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- MIDL do comutador/Char
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638636"
---
# <a name="char-switch"></a>comutador/Char

A opção **/Char** ajuda a garantir que o compilador de MIDL e o compilador C operem juntos corretamente para todos os tipos [**Char**](char-idl.md) e [**Small**](small.md) .

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>assinado * * * *


</dt> <dd>

Especifica que o tipo de compilador C padrão para [**Char**](char-idl.md) é assinado. Todas as ocorrências de **Char** não acompanhadas por uma especificação de sinal são geradas como caracteres não assinados.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>Não assinado * * * *


</dt> <dd>

Especifica que o tipo de compilador C padrão para [**Char**](char-idl.md) não é assinado. Todos os usos de [**pequenos**](small.md) não acompanhados por uma especificação de sinal são gerados como pequenos assinados.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7 * * * *


</dt> <dd>

Especifica que todos os valores de [**caracteres**](char-idl.md) devem ser passados para os arquivos gerados sem uma palavra-chave de assinatura específica. Todos os usos de [**pequenos**](small.md) não acompanhados por uma especificação de sinal são gerados como **pequenos**.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Por definição, o [**caractere**](char-idl.md) MIDL não é assinado. "Small" é definido em termos de **Char** ( \# define Small Char) e MIDL [**Small**](small.md) é assinado.

A opção **/Char** instrui o compilador MIDL a especificar declarações [**assinadas**](signed.md) explícitas ou [**sem sinal**](unsigned.md) nos arquivos gerados quando a declaração de assinatura do C-compilador estiver em conflito com o padrão MIDL para esse tipo.

Lembre-se de que o compilador MIDL gera os stubs como código-fonte C, que você deve compilar como parte de seus programas de cliente e servidor. Alguns compiladores usam um **caractere assinado** em todos os dados [**Char**](char-idl.md) especificados no código-fonte. O código-fonte do stub que o compilador MIDL gera trata todos os dados **Char** como **caracteres não assinados**. Se o compilador MIDL simplesmente gerar todos os dados **Char** no arquivo IDL como dados **Char** nos stubs, os compiladores que usam um **caractere assinado** para dados **Char** causarão um conflito no código-fonte do stub.

A finalidade da opção de linha de comando **/Char** é resolver esses conflitos em potencial. Preserva todos os dados especificados como [**Char**](char-idl.md) no arquivo IDL como um **caractere não assinado** no código-fonte do stub. Ele também mantém dados [**pequenos**](small.md) como assinados.

A tabela a seguir resume os tipos gerados.



| opção MIDL/Char       | Tipo de caractere gerado | Tipo pequeno gerado |
|-------------------------|---------------------|----------------------|
| **/Char de MIDL assinado**   | **unsigned char**   | **small**            |
| **MIDL/Char não assinado** | **char**            | **pequeno assinado**     |
| **/Char MIDL ascii7**   | **char**            | **small**            |



 

A opção **/Char** signed indica que o caractere do compilador C e os tipos pequenos são assinados. Para corresponder o padrão MIDL para **Char**, o compilador MIDL deve converter todos os usos de **Char** não acompanhados por uma especificação de sinal para um **Char não assinado**. O tipo [**pequeno**](small.md) não é modificado porque o padrão C-Compiler corresponde ao padrão MIDL para **pequeno**.

A opção **/Char** não assinado indica que o tipo de [**caractere**](char-idl.md) do compilador C não está assinado. O compilador MIDL converte todos os usos de [**pequenos**](small.md) não acompanhados por uma especificação de sinal para uma **assinatura** **pequena**.

A opção ascii7 indica que nenhuma especificação de sinal explícita é adicionada aos tipos [**Char**](char-idl.md) . O tipo [**pequeno**](small.md) é gerado como **pequeno**.

Para evitar confusão, você deve usar especificações de assinatura explícitas para tipos [**Char**](char-idl.md) e Small, sempre que possível no arquivo IDL. Observe que o uso de tipos de **caracteres** explicitamente assinados em seu arquivo IDL não é suportado pela DCE IDL. Portanto, esse recurso não está disponível quando você compila com a opção MIDL [**/OSF**](-osf.md)

Para obter mais informações relacionadas ao **/Char**, consulte [**Small**](small.md).

## <a name="examples"></a>Exemplos

**MIDL/Char assinou filename. idl**

**MIDL/Char filename não assinado. idl**

**MIDL/Char ascii7 filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**menores**](small.md)
</dt> </dl>

 

 




