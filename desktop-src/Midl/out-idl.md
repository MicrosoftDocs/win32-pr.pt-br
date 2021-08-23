---
title: atributo out
description: O atributo \ out \ identifica os parâmetros de ponteiro que são retornados do procedimento chamado para o procedimento de chamada (do servidor para o cliente).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- MIDL do atributo out
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32bdbd18c6412f943a124a62badb9c154fa9aeb64573919970ffc1dc4af17798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066796"
---
# <a name="out-attribute"></a>atributo out

O \[  \] atributo out identifica os parâmetros de ponteiro que são retornados do procedimento chamado para o procedimento de chamada (do servidor para o cliente).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são \[ [**retorno de chamada**](callback.md) \] , \[ [**local**](local.md) \] ; o atributo de ponteiro \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] ou \[ [**PTR**](ptr.md) \] ; e a cadeia de caracteres de atributos de uso \[ [](string.md) \] , \[ [**ignorar**](ignore.md) \] e \[ [**\_ identificador de contexto**](context-handle.md) \] .

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo de [base \_](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador de ponteiro* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Especifica zero ou mais atributos apropriados para um tipo de parâmetro especificado. Atributos de parâmetro com o \[ atributo **out** \] também podem pegar o atributo direcional \[ **out** \] ; os atributos Field \[ [**First \_ são**](first-is.md) \] , \[ [**Last \_ is**](last-is.md) \] , \[ [**length \_ is**](length-is.md) \] , \[ [**Max \_ is**](max-is.md) \] , \[ [**Size \_ is**](size-is.md) \] e \[ [**switch \_ Type**](switch-type.md) \] ; o atributo ponteiro \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] ou \[ [**PTR**](ptr.md) \] ; e o \[ [**\_ identificador de contexto**](context-handle.md) e a cadeia de \] \[ [**caracteres**](string.md) \] de atributos de uso. O atributo de uso \[ [**ignore**](ignore.md) \] não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> <dt>

*Declarador* 
</dt> <dd>

Especifica os declaradores padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \[  \] atributo out indica que um parâmetro que atua como um ponteiro e seus dados associados na memória são passados de volta do procedimento chamado para o procedimento de chamada.

O \[ atributo **out** \] deve ser um ponteiro. Os compiladores de IDL do DCE exigem a presença de um \* Declarador de ponteiro explícito na declaração de parâmetro. O Microsoft IDL oferece uma extensão que descarta esse requisito e permite uma matriz ou um tipo de ponteiro definido anteriormente.

Um atributo relacionado, \[ [**no**](in.md) \] , indica que o parâmetro é passado do procedimento de chamada para o procedimento chamado. Os \[  \] atributos in e \[ **out** \] especificam a direção na qual os parâmetros são passados. Um parâmetro pode ser definido como \[ somente **entrada**, \] \[ somente **out** \] ou \[ **in**, **out** \] .

Um \[  \] parâmetro out-only é considerado indefinido quando o procedimento remoto é chamado e a memória do objeto é alocada pelo servidor. Como os parâmetros/ponteiros de nível superior sempre devem apontar para um armazenamento válido e, portanto, não podem ser **nulos**, \[  \] não podem ser aplicados a ponteiros de nível superior \[ [](unique.md) \] ou \[ [**PTR**](ptr.md) \] . Parâmetros que são \[  \] ponteiros exclusivos ou \[ **PTR** \] devem estar \[ [**no**](in.md) \] ou \[ **nos** parâmetros de **saída** \] .

## <a name="examples"></a>Exemplos

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**Strings**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 