---
title: Atributo size_is
description: Use o atributo \ size is\ para especificar o tamanho da memória, em elementos, alocados para ponteiros dimensionados, ponteiros dimensionados para ponteiros dimensionados e matrizes \_ multidimensionais ou individuais.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is atributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd57748d3ad92407fd65f3a6af7fc1ebb68321b576d57a50b6ba6f5546f8d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066696"
---
# <a name="size_is-attribute"></a>size \_ é atributo

Use o atributo size is para especificar o tamanho da memória, em elementos, alocado para ponteiros dimensionados, ponteiros dimensionados para ponteiros dimensionados e matrizes \[ **\_** multidimensionais ou \] individuais.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica uma ou mais expressões da linguagem C. Cada expressão é avaliada como um inteiro não negativo que representa a quantidade de memória alocada para um ponteiro dimensionado ou uma matriz. No caso de uma matriz, especifica uma única expressão que representa o tamanho da alocação, em elementos, da primeira dimensão dessa matriz. O compilador MIDL dá suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decremento. Use vírgulas como espaço reservado para parâmetros implícitos ou para separar várias expressões.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você estiver usando o atributo size for para alocar memória para uma matriz multidimensional e estiver usando a notação de matriz, tenha em mente que apenas a primeira dimensão de uma matriz \[ **\_** \] \[ multidimensional pode ser determinada dinamicamente em tempo de \] executar. As outras dimensões devem ser especificadas estaticamente. Para obter mais informações sobre como usar o tamanho é o atributo com vários níveis de ponteiros para permitir que um servidor retorne uma matriz de dados de tamanho dinâmico para um cliente, conforme mostrado no proc7 de exemplo, consulte Vários níveis de \[ **\_** \] [ponteiros](/windows/desktop/Rpc/multiple-levels-of-pointers).

Você pode usar \[ **o tamanho \_ é** ou \] max [**\_ é**](max-is.md) (mas não ambos na mesma lista de atributos) para especificar o tamanho de uma matriz cujos limites superiores são determinados em tempo de executar. Observe, no entanto, que \[ **o atributo size \_ is** \] não pode ser usado em dimensões de matriz fixas. O \[ **atributo max \_ is** \] especifica o índice máximo de matriz válido. Como resultado, especificar size is(n) é equivalente a especificar \[ max \_ \] \[ \_ is(n-1) \] .

Um parâmetro de matriz compatível de dentro ou para dentro com o atributo de cadeia de caracteres não precisa \[ [](in.md) \] \[ ter o [](out-idl.md) \] tamanho \[ [](string.md) \] \[ **\_ é** \] ou max \[ [**\_ é**](max-is.md) \] atributo. Nesse caso, o tamanho da alocação é determinado do terminador NULL da cadeia de caracteres de entrada. Todas as outras matrizes compatíveis com o atributo \[ de \] cadeia de caracteres devem ter \[ **um tamanho \_ é** \] ou max \[ **\_ is** \] attribute.

Embora seja legal usar o atributo \[ **\_ size com** uma constante, isso é ineficiente e \] desnecessário. Por exemplo, use uma matriz de tamanho fixo:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

em vez de:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Você pode usar o \[ **tamanho é \_ e** \] o comprimento é \[ [**\_ atributos**](length-is.md) \] juntos. Quando você faz isso, \[ **o tamanho é \_ atributo** \] controla a quantidade de memória alocada para os dados. O \[ **atributo length \_ é** \] especifica quantos elementos são transmitidos. A quantidade de memória especificada pelo tamanho é e o comprimento dos atributos não precisa ser \[ **\_** \] o \[ **\_** \] mesmo. Por exemplo, seu cliente pode passar um parâmetro in,out para um servidor e especificar uma alocação de memória grande com tamanho é , mesmo que ele especifique um pequeno número de elementos de dados a serem passados com comprimento \[ \] \[ **\_** \] \[ **\_ é** \] . Isso permite que o servidor preencha a matriz com mais dados do que recebeu, que ele pode enviar de volta ao cliente.

Em geral, não é útil especificar que o \[ **tamanho \_ é** e \] o comprimento está \[ [**\_**](length-is.md) \] nos \[ \] parâmetros in ou \[ \] out. Em ambos os casos, \[ **size é \_ controles** \] de alocação de memória. Seu aplicativo pode usar size para alocar mais elementos de matriz do que \[ **\_** \] transmite (conforme especificado por \[ **comprimento \_ é** \] ). No entanto, isso seria ineficiente. Também seria ineficiente especificar valores idênticos para \[ **tamanho \_ e** \] tamanho \[ **\_ é** \] . Isso criaria sobrecarga extra durante o marshaling de parâmetros. Se os valores de \[ **tamanho \_ for** \] e length \[ **\_ for** \] sempre o mesmo, omitir o \[ **comprimento \_ será** \] atributo.

## <a name="examples"></a>Exemplos

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Em**](in.md)
</dt> <dt>

[**o último \_ é**](last-is.md)
</dt> <dt>

[**length \_ é**](length-is.md)
</dt> <dt>

[**max \_ é**](max-is.md)
</dt> <dt>

[**min \_ é**](min-is.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**String**](string.md)
</dt> </dl>

 

 