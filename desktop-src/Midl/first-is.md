---
title: Atributo first_is
description: O atributo \ \_ first is\ especifica o índice do primeiro elemento de matriz a ser transmitido.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is atributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d08be3ce14074c126a35272ede1b670121634f75d0b3d6cfb0db34e4f305760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067276"
---
# <a name="first_is-attribute"></a>primeiro \_ é o atributo

O \[ **primeiro \_ atributo** \] é especifica o índice do primeiro elemento de matriz a ser transmitido.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica uma ou mais expressões da linguagem C. Cada expressão é avaliada como um inteiro que representa o índice de matriz do primeiro elemento de matriz a ser transmitido. O compilador MIDL dá suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decremento. Separe várias expressões com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o **\[ primeiro atributo \_ for \]** não estiver presente ou se o índice especificado for um número negativo, o elemento de matriz zero será o primeiro elemento transmitido.

O **\[ primeiro atributo \_ é \]** também pode ajudar a determinar os valores dos índices de matriz correspondentes ao último é ou o atributo length é quando esses atributos não **\[** [**\_**](last-is.md) são **\]** **\[** [**\_**](length-is.md) **\]** especificados. A relação entre esses índices de matriz é:

``` syntax
length = last - first + 1
```

A seguinte relação também deve conter:

``` syntax
0 <= first_is <= max_is
```

A seguinte relação deve conter quando **\[** [**max é \_ <**](max-is.md) **\] = 0:**

``` syntax
first_is == 0
```

O **\[ primeiro atributo \_ é \]** não pode ser usado ao mesmo tempo que o atributo **\[** [**de cadeia de**](string.md) **\]** caracteres.

Usar uma expressão constante com **\[ o primeiro atributo \_ é \]** um uso inadequado do atributo. É legal, mas ineficiente e resultará em código de marshaling mais lento.

## <a name="examples"></a>Exemplos

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[atributos \_ de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**o último \_ é**](last-is.md)
</dt> <dt>

[**length \_ é**](length-is.md)
</dt> <dt>

[**max \_ é**](max-is.md)
</dt> <dt>

[**min \_ é**](min-is.md)
</dt> <dt>

[**size \_ é**](size-is.md)
</dt> <dt>

[**String**](string.md)
</dt> </dl>

 

 