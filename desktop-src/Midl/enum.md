---
title: atributo de enumeração
description: A palavra-chave enum identifica um tipo enumerado.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- atributo de enumeração MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1519e6208e8bccae0288d6e0b31d7897faba4e1c9c7add8987f5dd493f4f5f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384485"
---
# <a name="enum-attribute"></a>atributo de enumeração

A palavra-chave **enum** identifica um tipo enumerado.

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tags* 
</dt> <dd>

Especifica uma marca opcional para o tipo enumerado.

</dd> <dt>

*identifier* 
</dt> <dd>

Especifica a enumeração específica.

</dd> <dt>

*valor inteiro* 
</dt> <dd>

Especifica um valor inteiro constante.

</dd> </dl>

## <a name="remarks"></a>Comentários

os tipos de **Enumeração** podem aparecer como especificadores de tipo em declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como o tipo de retorno de função ou como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

No modo padrão do compilador de MIDL, você pode atribuir valores inteiros a enumeradores. (Esse recurso não está disponível quando você compila com o comutador [**/OSF**](-osf.md) .) Assim como acontece com enumeradores de linguagem C, os nomes de enumeradores devem ser exclusivos, mas os valores do enumerador não precisam ser.

Quando os operadores de atribuição não são fornecidos, os identificadores são mapeados para inteiros consecutivos da esquerda para a direita, começando com zero. Quando operadores de atribuição são fornecidos, os valores atribuídos começam do valor atribuído mais recentemente.

O número máximo de identificadores é 65.535.

Objetos do tipo **enum** são tipos [**int**](int.md) , e seu tamanho depende do sistema. Por padrão, os objetos de tipos **enum** são tratados como objetos de 16 bits do tipo [**sem sinal**](unsigned.md) [**curto**](short.md) quando transmitidos por uma rede. Os valores fora do intervalo 0-32.767 causam o \_ valor de enumeração RPC X da exceção \_ de tempo de execução \_ \_ fora \_ do \_ intervalo. Para transmitir objetos como entidades de 32 bits, aplique o **\[** atributo de [**\_ Enumeração v1**](v1-enum.md) **\]** ao typedef de **Enumeração** .

## <a name="examples"></a>Exemplos

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[**\_Enumeração v1**](v1-enum.md)
</dt> </dl>

 

 




