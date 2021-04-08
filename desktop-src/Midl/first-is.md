---
title: Atributo first_is
description: O atributo \ First \_ is \ especifica o índice do primeiro elemento de matriz a ser transmitido.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is do atributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823766"
---
# <a name="first_is-attribute"></a>primeiro \_ atributo é

O \[ **primeiro atributo \_ is** \] especifica o índice do primeiro elemento de matriz a ser transmitido.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de expressões limitadas* 
</dt> <dd>

Especifica uma ou mais expressões de linguagem C. Cada expressão é avaliada como um inteiro que representa o índice de matriz do primeiro elemento de matriz a ser transmitido. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo. Separe várias expressões com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o **\[ primeiro \_ atributo \] for** não estiver presente, ou se o índice especificado for um número negativo, o elemento de matriz zero será o primeiro elemento transmitido.

O **\[ primeiro \_ atributo \] is** também pode ajudar a determinar os valores dos índices de matriz correspondentes ao **\[** atributo [**Last \_ is**](last-is.md) **\]** ou **\[** [**length \_**](length-is.md) , **\]** quando esses atributos não são especificados. A relação entre esses índices de matriz é:

``` syntax
length = last - first + 1
```

A relação a seguir também deve conter:

``` syntax
0 <= first_is <= max_is
```

A relação a seguir deve ser mantida quando **\[** [**Max \_ é**](max-is.md) **\] <= 0:**

``` syntax
first_is == 0
```

O **\[ primeiro \_ atributo \] is** não pode ser usado ao mesmo tempo que o **\[** atributo de [**cadeia de caracteres**](string.md) **\]** .

O uso de uma expressão constante com o **\[ primeiro atributo \_ é \]** um uso inadequado do atributo. É legal, mas ineficiente, e resultará em um código de marshaling mais lento.

## <a name="examples"></a>Exemplos

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[atributos de campo \_](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**mín. \_ é**](min-is.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 