---
title: atributo de struct
description: A palavra-chave struct é usada em um especificador de tipo de estrutura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- MIDL do atributo struct
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105770389"
---
# <a name="struct-attribute"></a>atributo de struct

A palavra-chave **struct** é usada em um especificador de tipo de estrutura.

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*struct-tag* 
</dt> <dd>

Especifica uma marca opcional para a estrutura.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam ao membro da estrutura. Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último é \_**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md), **\]** **\[** [**Max \_ is**](max-is.md) **\]** e **\[** [**Size \_ is**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** e **\[** [**ignore**](ignore.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** . Separe vários atributos de campo com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo de [base](midl-base-types.md), **struct**, [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O especificador de tipo de estrutura IDL, **struct**, difere do especificador de tipo C padrão das seguintes maneiras:

-   Cada membro da estrutura pode ser associado a atributos de campo opcionais que descrevem características desse membro da estrutura para fins de uma chamada de procedimento remoto.
-   Os campos de bits e os declaradores de função não são permitidos em estruturas que são usadas em chamadas de procedimento remoto. Essas construções de Declarador C padrão só poderão ser usadas se a estrutura não for transmitida na rede.

A forma das estruturas deve ser a mesma entre as plataformas para garantir a interconectividade.

## <a name="examples"></a>Exemplos

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz e de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 