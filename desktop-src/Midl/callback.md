---
title: atributo de retorno de chamada
description: O atributo \ callback \ declara uma função de retorno de chamada estática que existe no lado do cliente do aplicativo distribuído. As funções de retorno de chamada fornecem uma maneira para o servidor executar código no cliente.
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
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365950"
---
# <a name="callback-attribute"></a>atributo de retorno de chamada

O atributo de **\[ retorno de chamada \]** declara uma função de retorno de chamada estática que existe no lado do cliente do aplicativo distribuído. As funções de retorno de chamada fornecem uma maneira para o servidor executar código no cliente.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*função-attr-lista* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [ \_ tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador de PTR* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado. Separe vários atributos com vírgulas.

</dd> <dt>

*Declarador* 
</dt> <dd>

Especifica um Declarador C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). O identificador de nome de parâmetro é opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função de **\[ retorno de chamada \]** é útil quando o servidor deve obter informações do cliente. Se os aplicativos de servidor tiverem suporte no Windows 3. *x*, o servidor pode fazer uma chamada para um procedimento remoto no Windows 3. *x* Server para obter as informações necessárias. A função de retorno de chamada realiza a mesma finalidade e permite que o servidor consulte o cliente para obter informações no contexto da chamada original.

Os retornos de chamada são casos especiais de chamadas remotas que são executadas como parte de um único thread. Um retorno de chamada é emitido no contexto de uma chamada remota. Qualquer procedimento remoto definido como parte da mesma interface que a função de retorno de chamada estática pode chamar a função de retorno de chamada.

É importante observar que o uso de retorno de \[ chamada \] não é recomendado na programação de vários threads. Como uma função de programação de thread único, ele não está equipado para dar suporte às demandas de segurança que um ambiente de vários threads fornece.

A função **RpcCancelThread** não pode ser usada para cancelar uma chamada que pode enviar um retorno de chamada estático. Se uma chamada de procedimento remoto específica nunca resultar em um retorno de chamada, ela poderá ser cancelada. Caso contrário, uma chamada poderá ser cancelada somente se puder ter certeza de que um retorno de chamada para ele não foi emitido.

Somente as sequências orientadas a conexão e de protocolo local dão suporte ao atributo de retorno de chamada. O tamanho dos \[ dados de saída \] para retornos de chamada na sequência de protocolo local é limitado a 150 bytes. Se uma interface RPC usar uma sequência de protocolo sem conexão (datagrama), as chamadas para procedimentos com o atributo de retorno de chamada falharão.

Identificadores não podem ser usados como parâmetros em funções de retorno de chamada. Como os retornos de chamadas são sempre executados no contexto de uma chamada, o identificador de associação usado pelo cliente para fazer a chamada para o servidor também é usado como o identificador de ligação do servidor para o cliente.

Os retornos de chamada podem ser aninhados em qualquer profundidade.

## <a name="examples"></a>Exemplos

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 