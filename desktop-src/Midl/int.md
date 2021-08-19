---
title: Atributo int
description: A palavra-chave int especifica um inteiro com sinal de 32 bits em plataformas de 32 bits. Em plataformas de 16 bits, a palavra-chave int é uma palavra-chave opcional que pode acompanhar as palavras-chave pequenas, curtas e longas.
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
ms.openlocfilehash: 640eae8bfbadcba07f67d244edd78726269ede9eee2f14e9af06e851bb5cac92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807194"
---
# <a name="int-attribute"></a>Atributo int

A **palavra-chave int** especifica um inteiro com sinal de 32 bits em plataformas de 32 bits. Em plataformas de 16 bits, a palavra-chave **int** é uma palavra-chave opcional que pode acompanhar as palavras-chave [**small,**](small.md) [**short**](short.md)e [**long.**](long.md)

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*modificador de inteiro* 
</dt> <dd>

Especifica a palavra-chave [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)ou [**\_ \_ int64**](--int64.md), que seleciona o tamanho dos dados inteiros. Em plataformas de 16 bits, o qualificador de tamanho deve estar presente.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Declaradores de função e declarações de campo de bits não são permitidos em estruturas transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os tipos inteiros estão entre os tipos base da IDL (linguagem de definição de interface). Eles podem aparecer como especificadores de tipo em declarações [**typedef,**](typedef.md) declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [Arquivo de definição de interface (IDL).](interface-definition-idl-file.md)

Se nenhuma especificação de sinal de inteiro for fornecida, o tipo inteiro assume como padrão [**assinado**](signed.md).

Os compiladores de IDL de DCE não permitem que a palavra-chave [**assinada**](signed.md) especifique o sinal de tipos inteiros. Portanto, esse recurso não está disponível quando você usa a opção [**/osf do**](-osf.md) compilador MIDL.

A Microsoft não recomenda o uso \_ \_ de int3264 para a remoção, se puder ser evitada. Consulte o tópico sobre [**\_ \_ int3264 para**](--int3264.md) obter mais informações sobre seu uso e limitações.

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

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Assinado**](signed.md)
</dt> <dt>

[**Pequeno**](small.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**União**](union.md)
</dt> </dl>

 

 




