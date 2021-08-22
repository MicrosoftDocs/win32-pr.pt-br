---
title: context_handle_noserialize atributo
description: O atributo \context \_ handle noserialize\ ACF garante que um handle de contexto nunca será serializado, independentemente do \_ comportamento padrão do aplicativo.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40556db0d63441e42d46a0ed7f9bd45edb8b2ce65f8d4b9b84e3a848325ddbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013994"
---
# <a name="context_handle_noserialize-attribute"></a>atributo \_ context handle \_ naerialize

O **\[ atributo \_ \_ ACF \] de naerialização** do handle de contexto garante que um handle de contexto nunca será serializado, independentemente do comportamento padrão do aplicativo.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Todos os outros atributos do ACF que se aplicam ao tipo.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

O identificador que especifica o tipo de identificador de contexto, conforme definido em uma declaração [**typedef.**](typedef.md) Esse é o tipo que recebe o atributo [**\[ de \_ identificador de \]**](context-handle.md) contexto no arquivo IDL.

</dd> <dt>

*function-acf-attribute-list* 
</dt> <dd>

Quaisquer atributos ACF adicionais que se aplicam à função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

O nome da função conforme definido no arquivo IDL.

</dd> <dt>

*parameter-acf-attribute-list* 
</dt> <dd>

Quaisquer outros atributos do ACF que se aplicam ao parâmetro .

</dd> <dt>

*param-name* 
</dt> <dd>

O nome do parâmetro conforme definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O [**\[ atributo de \_ identificador \]**](context-handle.md) de contexto identifica um identificador de associação que mantém informações de contexto ou de estado no servidor entre chamadas de procedimento remoto. O atributo pode aparecer como um atributo de tipo [**typedef**](typedef.md) IDL, como um atributo de tipo de retorno de função ou como um atributo de parâmetro.

Por padrão, chamadas em alças de contexto são serializadas. Um aplicativo pode chamar [**RpcSsDontSerializeContext para**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) substituir esse comportamento padrão. O uso [**\[ do atributo \_ de \]**](context-handle.md) alça de contexto em um arquivo ACF garante que as chamadas nesse determinado alçamento de contexto não serão serializadas, independentemente do comportamento do aplicativo de chamada. Fornecer uma rotina de rundown de contexto é opcional.

Esse atributo está disponível no MIDL versão 5.0.

**Windows ServerÂ 2003 e Windows XP ou posterior:** Uma única interface pode acomodar as alças de contexto serializadas e não serializadas, permitindo que um método em uma interface acesse um handle de contexto exclusivamente (serializado), enquanto outros métodos acessam esse lidar de contexto no modo compartilhado (não serializado). Esses recursos de acesso são comparáveis aos mecanismos de bloqueio de leitura/gravação; métodos que usam um alça de contexto serializado são usuários exclusivos (autores), enquanto os métodos que usam um alça de contexto não serializado são usuários compartilhados (leitores). Os métodos que destrói ou modificam o estado de um alça de contexto devem ser serializados. Métodos que não modificam o estado de um handle de contexto, como os métodos que simplesmente leem de um handle de contexto, podem ser não desselizados. Observe que os métodos de criação são serializados implicitamente.

## <a name="examples"></a>Exemplos

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos do ACF](acf-attributes.md)
</dt> <dt>

[**serializar \_ o \_ alça de contexto**](context-handle-serialize.md)
</dt> <dt>

[**alça de \_ contexto**](context-handle.md)
</dt> <dt>

[Alças de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Rotina de run-down do contexto do servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Clientes multithread e alças de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 