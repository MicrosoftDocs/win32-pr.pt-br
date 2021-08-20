---
title: atributo de retorno de chamada
description: O atributo \ retorno de chamada\ declara uma função de retorno de chamada estática que existe no lado do cliente do aplicativo distribuído. As funções de retorno de chamada fornecem uma maneira para o servidor executar o código no cliente.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- atributo de retorno de chamada MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77eb93a78553ccbc95b1671dc215012eeccc56b0bff8ea23e47f68aaf51e10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807332"
---
# <a name="callback-attribute"></a>atributo de retorno de chamada

O **\[ atributo \] de retorno** de chamada declara uma função de retorno de chamada estática que existe no lado do cliente do aplicativo distribuído. As funções de retorno de chamada fornecem uma maneira para o servidor executar o código no cliente.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*function-attr-list* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função **\[** [**válidos são locais**](local.md); o atributo de ponteiro ref , exclusivo ou ptr ; e a cadeia de caracteres de atributos de uso **\]** , **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [](string.md) **\]** **\[** [**ignoram**](ignore.md)e o indicador de **\]** **\[** [**\_ contexto**](context-handle.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo base , [**struct**](struct.md), [**union**](union.md), [**tipo enum**](enum.md) ou identificador de tipo. [ \_](midl-base-types.md) Uma especificação de armazenamento opcional pode *preceder o especificador de tipo*.

</dd> <dt>

*ptr-declarator* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um declarador de ponteiro é o mesmo que o declarador de ponteiro usado em C; ele é construído a partir do \* designador, modificadores como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado. Separe vários atributos com vírgulas.

</dd> <dt>

*Declarador* 
</dt> <dd>

Especifica um declarador C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, [consulte Matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). O identificador de nome de parâmetro é opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\[ função \] de retorno** de chamada é útil quando o servidor deve obter informações do cliente. Se os aplicativos de servidor fossem suportados Windows 3. *x*, o servidor pode fazer uma chamada para um procedimento remoto no Windows 3. *x* server para obter as informações necessárias. A função de retorno de chamada realiza a mesma finalidade e permite que o servidor consulte o cliente para obter informações no contexto da chamada original.

Retornos de chamada são casos especiais de chamadas remotas que são executados como parte de um único thread. Um retorno de chamada é emitido no contexto de uma chamada remota. Qualquer procedimento remoto definido como parte da mesma interface que a função de retorno de chamada estática pode chamar a função de retorno de chamada.

É importante observar que o uso de \[ retorno de chamada não é recomendado na programação de vários \] threads. Como uma função de programação de thread único, ela não é equipado para dar suporte às demandas de segurança que um ambiente de vários threads fornece.

A **função RpcCancelThread** não pode ser usada para cancelar uma chamada que pode expedir um retorno de chamada estático. Se uma chamada de procedimento remoto específica nunca resultar em um retorno de chamada, ela poderá ser cancelada. Caso contrário, uma chamada poderá ser cancelada somente se for possível garantir que um retorno de chamada para ela não tenha sido emitido.

Somente as sequências de protocolo local e orientadas a conexão suportam o atributo de retorno de chamada. O tamanho dos dados \[ de saída para retornos de chamada na sequência de protocolo local é limitado a \] 150 bytes. Se uma interface RPC usar uma sequência de protocolo sem conexão (datagrama), as chamadas para procedimentos com o atributo de retorno de chamada falharão.

Os alças não podem ser usados como parâmetros em funções de retorno de chamada. Como os retornos de chamada sempre são executados no contexto de uma chamada, o handle de associação usado pelo cliente para fazer a chamada ao servidor também é usado como o handle de associação do servidor para o cliente.

Os retornos de chamada podem aninhar a qualquer profundidade.

## <a name="examples"></a>Exemplos

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**alça de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**União**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 