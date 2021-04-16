---
title: context_handle_serialize atributo
description: O atributo \ Context \_ Handlers \_ SERIALIZE \ ACF garante que um identificador de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize do atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758783"
---
# <a name="context_handle_serialize-attribute"></a>\_ \_ atributo serializar identificador de contexto

Os **\[ \_ identificadores de contexto \_ serializam \]** o atributo ACF garante que um identificador de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo-ACF-lista de atributos* 
</dt> <dd>

Quaisquer outros atributos de ACF que se aplicam ao tipo.

</dd> <dt>

*tipo de identificador de contexto* 
</dt> <dd>

O identificador que especifica o tipo de identificador de contexto, conforme definido em uma declaração de [**typedef**](typedef.md) . Esse é o tipo que recebe o atributo de **\[ \_ \_ serialização \] de identificador de contexto** no arquivo IDL.

</dd> <dt>

*função-ACF-atributo-List* 
</dt> <dd>

Quaisquer atributos adicionais do ACF que se aplicam à função.

</dd> <dt>

*nome da função* 
</dt> <dd>

O nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*parâmetro-ACF-lista de atributos* 
</dt> <dd>

Quaisquer outros atributos de ACF que se aplicam ao parâmetro.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

O nome do parâmetro, conforme definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ \_ \_ serializar \] identificador de contexto** identifica um identificador de associação que mantém informações de contexto ou estado no servidor entre chamadas de procedimento remoto. O atributo pode aparecer como um atributo de tipo de [**typedef**](typedef.md) de IDL, como um atributo de tipo de retorno de função ou como um atributo de parâmetro.

Por padrão, as chamadas em identificadores de contexto são serializadas, mas um aplicativo pode chamar [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para substituir esse comportamento padrão. Usar o atributo de **\[ \_ \_ serialização \] de identificador de contexto** em um arquivo ACF garante que as chamadas nesse identificador de contexto específico serão serializadas, mesmo que o aplicativo de chamada tenha substituído a serialização padrão. Uma rotina de encerramento de contexto é opcional.

Esse atributo está disponível no MIDL versão 5,0.

**Windows Server ServerÂ 2003 e WINDOWSÂ XP ou posterior:** Uma única interface pode acomodar identificadores de contexto serializados e não serializados, permitindo que um método em uma interface acesse um identificador de contexto exclusivamente (serializado), enquanto outros métodos acessam esse identificador de contexto no modo compartilhado (não serializado). Esses recursos de acesso são comparáveis a mecanismos de bloqueio de leitura/gravação; os métodos que usam um identificador de contexto serializado são usuários exclusivos (gravadores), enquanto os métodos que usam um identificador de contexto não serializado são usuários compartilhados (leitores). Os métodos que destruim ou modificam o estado de um identificador de contexto devem ser serializados. Os métodos que não modificam o estado de um identificador de contexto, como os métodos que simplesmente lêem de um identificador de contexto, podem ser não serializados. Observe que os métodos de criação são serializados implicitamente.

## <a name="examples"></a>Exemplos

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Atributos de ACF](acf-attributes.md)
</dt> <dt>

[**identificador de contexto \_ \_ noserializeize**](context-handle-noserialize.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Rotina de execução de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Clientes multithread e identificadores de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 