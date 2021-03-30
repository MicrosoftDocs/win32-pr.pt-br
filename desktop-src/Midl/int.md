---
title: atributo int
description: A palavra-chave int especifica um número inteiro com sinal de 32 bits em plataformas de 32 bits. Em plataformas de 16 bits, a palavra-chave int é uma palavra-chave opcional que pode acompanhar as palavras-chaves pequenas, curtas e longas.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- atributo int MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638423"
---
# <a name="int-attribute"></a>atributo int

A palavra-chave **int** especifica um número inteiro com sinal de 32 bits em plataformas de 32 bits. Em plataformas de 16 bits, a palavra-chave **int** é uma palavra-chave opcional que pode acompanhar as palavras-chaves [**pequenas**](small.md), [**curtas**](short.md)e [**longas**](long.md).

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*modificador de número inteiro* 
</dt> <dd>

Especifica a palavra-chave [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)ou [**\_ \_ Int64**](--int64.md), que seleciona o tamanho dos dados inteiros. Em plataformas de 16 bits, o qualificador de tamanho deve estar presente.

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os tipos de inteiros estão entre os tipos base da IDL (Interface Definition Language). Eles podem aparecer como especificadores de tipo em declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

Se nenhuma especificação de sinal de inteiro for fornecida, o tipo de inteiro padrão será [**assinado**](signed.md).

Os compiladores de IDL do DCE não permitem que a palavra-chave seja [**assinada**](signed.md) para especificar o sinal dos tipos inteiros. Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.

A Microsoft não recomenda o uso do \_ \_ int3264 para comunicação remota se puder ser evitada. Consulte o tópico em [**\_ \_ int3264**](--int3264.md) para obter mais informações sobre o uso e as limitações dele.

## <a name="examples"></a>Exemplos

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**inteiro**](signed.md)
</dt> <dt>

[**menores**](small.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unida**](union.md)
</dt> </dl>

 

 




