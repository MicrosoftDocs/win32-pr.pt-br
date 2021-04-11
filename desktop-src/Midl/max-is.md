---
title: Atributo max_is
description: O atributo \ Max \_ is \ designa o valor máximo para um índice de matriz válido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is do atributo MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293952"
---
# <a name="max_is-attribute"></a>\_atributo Max é

O atributo **\[ Max \_ é \]** designa o valor máximo para um índice de matriz válido.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de expressões limitadas* 
</dt> <dd>

Especifica uma ou mais expressões de linguagem C. Cada expressão é avaliada como um inteiro que representa o índice de matriz válido mais alto. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo. Separe várias expressões com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ Max \_ is \]** não corresponde necessariamente ao número de elementos na matriz. Para uma matriz de tamanho *n* em C, em que o primeiro elemento de matriz é o número de elemento zero, o valor máximo para um índice de matriz válido é *n*– 1.

O atributo **\[ Max \_ is \]** não pode ser usado como um atributo Field ao mesmo tempo que o **\[** [**tamanho \_ é**](size-is.md) **\]** Attribute.

Embora seja legal usar o atributo **\[ Max \_ is \]** com uma expressão constante, fazer isso é ineficiente e desnecessário. Por exemplo, use uma matriz de tamanho fixo:

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

em vez de:

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>Exemplos

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**mín. \_ é**](min-is.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> </dl>

 

 