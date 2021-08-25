---
title: atributo idempotente
description: O atributo \ idempotente \ especifica que uma operação não modifica informações de estado e retorna os mesmos resultados toda vez que é executada. Executar a rotina mais de uma vez tem o mesmo efeito que executá-la uma vez.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- MIDL de atributo idempotente
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a4135fdcb38fbad9e41b04a136f69420da7455f68d38a0c507135892e2a00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895216"
---
# <a name="idempotent-attribute"></a>atributo idempotente

O atributo **\[ idempotente \]** especifica que uma operação não modifica informações de estado e retorna os mesmos resultados toda vez que é executada. Executar a rotina mais de uma vez tem o mesmo efeito que executá-la uma vez.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica atributos adicionais a serem aplicados à função. Separe vários atributos com vírgulas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função à qual o atributo **\[ idempotente \]** será aplicado.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O RPC dá suporte a dois tipos de semântica de chamada remota: chamadas para operações com o atributo **\[ idempotente \]** e chamadas para operações (operações *idempotentes* ) sem o atributo **\[ idempotente \]** (operações *não idempotentes* ). Uma operação idempotente pode ser executada mais de uma vez sem nenhum efeito. Por outro lado, uma operação não idempotente não pode ser executada mais de uma vez, pois ela retornará resultados diferentes a cada vez ou, por isso, modificará algum estado.

Para garantir que um procedimento seja automaticamente executado novamente se a chamada não for concluída, use o atributo **\[ idempotente \]** . Se os atributos **\[ idempotente \]**, **\[** [**Broadcast**](broadcast.md) **\]** ou **\[** [**talvez**](maybe.md) **\]** não estiverem presentes, o procedimento usará semânticas não idempotentes por padrão. Nesse caso, a operação é executada apenas uma vez.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**difusor**](broadcast.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Eu**](maybe.md)
</dt> </dl>

 

 




