---
title: Atributo length_is
description: O atributo \ length \_ is \ especifica o número de elementos da matriz a serem transmitidos. Você deve especificar um valor não negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is do atributo MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454046"
---
# <a name="length_is-attribute"></a>comprimento \_ é atributo

O **\[ tamanho \_ é \]** atributo especifica o número de elementos da matriz a serem transmitidos. Você deve especificar um valor não negativo.

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de expressões limitadas* 
</dt> <dd>

Especifica uma ou mais expressões de linguagem C. Cada expressão é avaliada como um inteiro que representa o número de elementos da matriz a serem transmitidos. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo. Separe várias expressões com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ tamanho \_ é \]** o atributo determina o valor dos índices de matriz correspondentes ao **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** último atributo é quando o último não é especificado. A relação entre esses índices de matriz é a seguinte: comprimento = último-primeiro + 1.

O **\[ \_ tamanho \]** do atributo não pode ser usado ao mesmo tempo que o **\[** [**último \_**](last-is.md) atributo **\]** ou o atributo de **\[** [**cadeia de caracteres**](string.md) **\]** .

Para definir uma cadeia de caracteres contada com um **\[ comprimento \_ \]** ou **\[** o [**último \_ é**](last-is.md) **\]** atributo, use uma matriz de caracteres ou um ponteiro sem o atributo de cadeia de **\[** [**caracteres**](string.md) **\]** .

Usar uma expressão constante com o **\[ comprimento \_ é \]** o atributo é um uso inadequado do atributo. É legal, mas ineficiente, e resultará em um código de marshaling mais lento.

Você pode usar o **\[** [**tamanho \_**](size-is.md) **\]** e o **\[ comprimento \_ são \]** atributos juntos. Quando você fizer isso, o atributo **\[ Size \_ \]** controlará a quantidade de memória alocada para os dados. O **\[ tamanho \_ é \]** atributo especifica quantos elementos são transmitidos. A quantidade de memória especificada pelo **\[ tamanho \_ é \]** e o **\[ comprimento \_ \]** dos atributos não precisam ser iguais. Por exemplo, o cliente pode passar **um parâmetro \]** **\[ de entrada** para um servidor e especificar uma grande alocação de **\[ \_ \]** memória com tamanho, embora especifique um pequeno **\[ \_ \]** número de elementos de dados a serem passados com comprimento. Isso permite que o servidor preencha a matriz com mais dados do que ele recebeu, o que pode então enviar de volta para o cliente.

Em geral, não é útil especificar o **\[** [**tamanho \_**](size-is.md) **\]** e o **\[ comprimento \_ está \]** nos **\[** parâmetros [**in**](in.md) **\]** ou **\[** [**out**](out-idl.md) **\]** . Em ambos os casos, o **\[ tamanho \_ é \]** controlar a alocação de memória. Seu aplicativo pode usar o **\[ tamanho \_ \]** para alocar mais elementos de matriz do que transmitidos (conforme **\[ \_ \]** especificado pelo comprimento). No entanto, isso seria ineficiente. Também seria ineficiente especificar valores idênticos para o **\[ tamanho \_ \]** e o **\[ comprimento \_ é \]**. Porque ele criaria uma sobrecarga extra durante o marshaling do parâmetro. Quando os valores de **\[ tamanho \_ \]** e **\[ \_ \] comprimento** são sempre iguais, omita o **\[ comprimento \_ é \]** atributo.

## <a name="examples"></a>Exemplos

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**mín. \_ é**](min-is.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 