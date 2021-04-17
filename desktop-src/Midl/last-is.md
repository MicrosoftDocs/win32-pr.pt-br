---
title: Atributo last_is
description: O atributo Field \ Last \_ is \ especifica o índice do último elemento de matriz a ser transmitido. Quando o índice especificado é zero ou negativo, nenhum elemento de matriz é transmitido.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is do atributo MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499040"
---
# <a name="last_is-attribute"></a>último \_ atributo is

O atributo de campo **\[ Last \_ é \]** especifica o índice do último elemento de matriz a ser transmitido. Quando o índice especificado é zero ou negativo, nenhum elemento de matriz é transmitido.

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de expressões limitadas* 
</dt> <dd>

Especifica uma ou mais expressões de linguagem C. Cada expressão é avaliada como um inteiro que representa o índice de matriz do último elemento de matriz a ser transmitido. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo. Separe várias expressões com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ último \_ atributo \] is** determina o valor do índice de matriz correspondente ao **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** comprimento é o atributo quando length não é especificado. A relação entre esses índices de matriz é a seguinte: comprimento = último-primeiro + 1.

Se o valor do índice de matriz especificado pela **\[** [**primeira \_ for**](first-is.md) **\]** maior que o **\[ \_ \]** valor especificado pelo último, os elementos zero serão transmitidos.

O **\[ último \_ atributo \] is** não pode ser usado como um atributo de campo ao mesmo tempo que o **\[** [**comprimento \_ é**](length-is.md) um atributo **\]** ou o atributo de **\[** [**cadeia de caracteres**](string.md) **\]** .

O uso de uma expressão constante com o **\[ último atributo \_ é \]** um uso inadequado do atributo. É legal, mas ineficiente, e resultará em um código de marshaling mais lento.

Quando o valor especificado por **\[** [**Max \_ é**](max-is.md) **\]** igual ou maior que zero, a relação a seguir deve ser verdadeira: 0 <= Last \_ é <= Max \_ é.

## <a name="examples"></a>Exemplos

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> </dl>

 

 