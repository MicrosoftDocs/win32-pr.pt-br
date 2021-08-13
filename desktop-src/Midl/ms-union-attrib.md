---
title: Atributo ms_union
description: A palavra-chave \ ms union\ é usada para controlar o alinhamento \_ de NDR de uniões não truncadas.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union atributo MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 860054fe26657c4028c172da08e0c56dbf6ae257ffc98e79905f8420b54e6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642794"
---
# <a name="ms_union-attribute"></a>Atributo de \_ união ms

A \[ **palavra-chave ms \_ union** \] é usada para controlar o alinhamento de NDR de uniões não truncadas.

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*tipo de procedimento* 
</dt> <dd>

Especifica o tipo de retorno do procedimento ao qual o atributo está sendo aplicado.

</dd> <dt>

*nome do procedimento* 
</dt> <dd>

Especifica o nome do procedimento.

</dd> <dt>

*param-list* 
</dt> <dd>

Especifica a lista de parâmetros do procedimento, que pode estar vazia.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nunca use essa opção ou atributo com novas interfaces. Esse é apenas um recurso de compatibilidade com compatibilidade com backward. O compilador MIDL nesta versão do Microsoft RPC espelha o comportamento do compilador IDL de DCE do OSF para uniões não truncadas. No entanto, como versões anteriores do compilador MIDL não fizeram isso, a opção de união [**/ms \_**](-ms-union.md) fornece compatibilidade com interfaces criadas em versões anteriores do compilador MIDL.

O **recurso de \_ união ms** pode ser usado como um atributo de interface IDL, um atributo de tipo IDL ou como uma opção de linha de comando ( [**/ms \_ union**](-ms-union.md)).

## <a name="examples"></a>Exemplos

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**/ms \_ union**](-ms-union.md)
</dt> </dl>

 

 




