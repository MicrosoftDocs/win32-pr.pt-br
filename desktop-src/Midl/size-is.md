---
title: Atributo size_is
description: Use o atributo \ Size \_ is \ para especificar o tamanho da memória, em elementos, alocados para ponteiros de tamanho, ponteiros de tamanho para ponteiros de tamanho e matrizes de dimensão única ou multidimensionais.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is do atributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640511"
---
# <a name="size_is-attribute"></a>o tamanho \_ é atributo

Use o \[ **atributo \_ tamanho** \] para especificar o tamanho da memória, em elementos, alocados para ponteiros de tamanho, ponteiros de tamanho para ponteiros de tamanho e matrizes de dimensão única ou multidimensional.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de expressões limitadas* 
</dt> <dd>

Especifica uma ou mais expressões de linguagem C. Cada expressão é avaliada como um inteiro não negativo que representa a quantidade de memória alocada a um ponteiro de tamanho ou uma matriz. No caso de uma matriz, especifica uma única expressão que representa o tamanho da alocação, em elementos, da primeira dimensão dessa matriz. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo. Use vírgulas como espaços reservados para parâmetros implícitos ou para separar várias expressões.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você estiver usando o \[ **atributo \_ size** \] para alocar memória para uma matriz multidimensional e estiver usando a \[ \] notação de matriz, lembre-se de que apenas a primeira dimensão de uma matriz multidimensional pode ser determinada dinamicamente em tempo de execução. As outras dimensões devem ser especificadas estaticamente. Para obter mais informações sobre como usar o \[ **tamanho \_ é** o \] atributo com vários níveis de ponteiros para permitir que um servidor retorne uma matriz de dados de tamanho dinâmico para um cliente, como mostrado no exemplo Proc7, consulte [vários níveis de ponteiros](/windows/desktop/Rpc/multiple-levels-of-pointers).

Você pode usar o \[ **tamanho \_** \] ou o [**máximo \_ é**](max-is.md) (mas não ambos na mesma lista de atributos) para especificar o tamanho de uma matriz cujos limites superiores são determinados em tempo de execução. Observe, no entanto, que o \[ atributo **Size \_ is** \] não pode ser usado em dimensões de matriz que são fixas. O \[ atributo **Max \_ is** \] especifica o índice de matriz válido máximo. Como resultado, especificar \[ Size \_ é (n) \] equivale a especificar \[ Max \_ é (n-1) \] .

Um \[ [](in.md) \] parâmetro de \[ matriz em [](out-idl.md) \] conformidade com ou para fora, com o atributo de \[ [**cadeia de caracteres**](string.md) , \] não precisa ter o \[ **tamanho \_** \] ou o \[ atributo [**máximo \_ é**](max-is.md) \] . Nesse caso, o tamanho da alocação é determinado do terminador nulo da cadeia de caracteres de entrada. Todas as outras matrizes em conformidade com o \[ atributo de cadeia de caracteres \] devem ter um \[ atributo **Size \_** \] ou \[ **Max \_ is** \] .

Embora seja legal usar o \[ **tamanho \_** do \] atributo com uma constante, fazer isso é ineficiente e desnecessário. Por exemplo, use uma matriz de tamanho fixo:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

em vez de:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Você pode usar o \[ **tamanho \_** \] e o \[ [**comprimento \_ são**](length-is.md) \] atributos juntos. Quando você fizer isso, o \[ atributo **\_ size** \] controlará a quantidade de memória alocada para os dados. O \[ **tamanho \_ é** \] atributo especifica quantos elementos são transmitidos. A quantidade de memória especificada pelo \[ **tamanho \_ é** \] e o \[ **comprimento \_** dos \] atributos não precisam ser iguais. Por exemplo, o cliente pode passar um \[ parâmetro de entrada \] para um servidor e especificar uma grande alocação de memória com \[ **tamanho \_** \] , embora especifique um pequeno número de elementos de dados a serem passados com \[ **\_ comprimento** \] . Isso permite que o servidor preencha a matriz com mais dados do que ele recebeu, o que pode então enviar de volta para o cliente.

Em geral, não é útil especificar o \[ **tamanho \_** \] e o \[ [**comprimento \_ está**](length-is.md) \] nos \[ parâmetros in \] ou \[ out \] . Em ambos os casos, o \[ **tamanho \_ é** \] controlar a alocação de memória. Seu aplicativo pode usar o \[ **tamanho \_** \] para alocar mais elementos de matriz do que transmitidos (conforme especificado pelo \[ **comprimento \_** \] ). No entanto, isso seria ineficiente. Também seria ineficiente especificar valores idênticos para o \[ **tamanho \_** \] e o \[ **comprimento \_ é** \] . Ele criaria uma sobrecarga extra durante o marshaling do parâmetro. Se os valores de \[ **tamanho \_** \] e \[ **comprimento \_** \] forem sempre iguais, omita o \[ **comprimento \_ é** \] atributo.

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

[**Storage**](arrays-1.md)
</dt> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**mín. \_ é**](min-is.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 