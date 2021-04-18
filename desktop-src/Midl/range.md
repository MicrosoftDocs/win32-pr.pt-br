---
title: atributo de intervalo
description: O atributo \ Range \ permite especificar um intervalo de valores permitidos para argumentos ou campos cujos valores são definidos em tempo de execução. Quando usado com um tipo de pipe, o atributo especifica o intervalo permitido para a contagem de elementos nas partes do pipe.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- atributo de intervalo MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105787511"
---
# <a name="range-attribute"></a>atributo de intervalo

O atributo **\[ Range \]** permite especificar um intervalo de valores permitidos para argumentos ou campos cujos valores são definidos em tempo de execução. Quando usado com um tipo de pipe, o atributo especifica o intervalo permitido para a contagem de elementos nas partes do pipe.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor baixo* 
</dt> <dd>

O menor valor permitido que o parâmetro ou campo pode conter.

</dd> <dt>

*valor alto* 
</dt> <dd>

O valor mais alto permitido que o parâmetro ou campo pode conter.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Um tipo integral diferente de [**Hyper**](hyper.md) ou [**\_ \_ Int64**](--int64.md), um identificador de tipo para um tipo integral, um tipo de [**Enumeração**](enum.md) ou um nome de tipo de pipe.

</dd> <dt>

*Declarador* 
</dt> <dd>

Um Declarador C padrão, como um identificador.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ Range \]** para modificar o significado de parâmetros ou campos confidenciais, como aqueles usados para tamanho ou comprimento, com matrizes em conformidade ou variáveis; ou sempre que desejar verificar um parâmetro ou valor de campo em relação a um intervalo de valores válidos. O atributo é aplicável a parâmetros de nível superior, bem como a parâmetros e campos de nível inferior. A adição do atributo **\[ Range \]** a um tipo não altera seu formato de conexão, portanto, não afeta a compatibilidade com versões anteriores.

O atributo **\[ Range \]** também pode ser usado em dados em conformidade, como buffers ou matrizes com um atributo de compatibilidade. O efeito é limitar todos os tamanhos de conformidade para os dados de acordo com o intervalo especificado. Se os dados em conformidade forem uma matriz multidimensional, cada dimensão de matriz será limitada ao intervalo especificado.

O uso do **\[ intervalo \]** em dados em conformidade requer que o destino de compilação seja â € "Target NT60 ou superior.

Observe que você deve usar a opção de compilador [**/robust**](-robust.md) ao compilar o arquivo IDL para gerar o código de stub que executará essas verificações. Sem a opção **/robust** , o compilador MIDL ignora esse atributo.

## <a name="examples"></a>Exemplos

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[matrizes](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**switch \_ é**](switch-is.md)
</dt> </dl>

 

 