---
title: atributo de pipe
description: O construtor de tipo de pipe torna possível transmitir um fluxo aberto de dados digitados através de uma chamada de procedimento remoto.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- MIDL do atributo de pipe
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293935"
---
# <a name="pipe-attribute"></a>atributo de pipe

O construtor de tipo de **pipe** torna possível transmitir um fluxo aberto de dados digitados através de uma chamada de procedimento remoto.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de elemento* 
</dt> <dd>

Define o tamanho de um único elemento no buffer de transferência. O *tipo de elemento* pode ser um [tipo base](midl-base-types.md), um \_ tipo predefinido, um [**struct**](struct.md), uma [**Enumeração 32b**](v1-enum.md)ou um identificador de tipo. Várias restrições se aplicam a *\_ tipos de elementos*, conforme descrito em comentários, abaixo.

</dd> <dt>

*Declarador de pipe* 
</dt> <dd>

Especifica um ou mais identificadores ou ponteiros para identificadores. Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar o construtor de tipo de **pipe** para transmitir dados em ambas as direções. Um **\[** [](in.md) **\]** parâmetro no pipe permite que o servidor receba o fluxo de dados do cliente durante uma chamada de procedimento remoto. Um **\[** [](out-idl.md) **\]** parâmetro out pipe permite que o servidor envie por push o fluxo de dados de volta para o cliente. Você fornece as rotinas do lado do cliente para enviar por push e efetuar pull do fluxo de dados e alocar um buffer global para os dados. As rotinas de stub do cliente e do servidor realizam marshaling e unmarshaling de dados e transmitem uma referência para o buffer de volta para o aplicativo.

As seguintes restrições se aplicam a Pipes:

-   Um elemento de pipe não pode ser ou conter um ponteiro, uma matriz em conformidade ou variável, um identificador ou um identificador de contexto. Além disso, na implementação de pipes da Microsoft, um elemento de pipe não pode ser ou conter uma [**Union**](union.md), uma [**Enumeração 16B**](enum.md)ou um [**\_ \_ int3264**](--int3264.md).
-   Você não pode aplicar os **\[** atributos [**transmitir \_ como**](transmit-as.md) **\]** , **\[** [**representar \_ como**](represent-as.md) **\]** , **\[** [**\_ realizar marshaling**](wire-marshal.md) **\]** ou **\[** [**\_ Marshal do usuário**](user-marshal.md) **\]** a um tipo de pipe ou ao *tipo de elemento*.
-   Um tipo de pipe não pode ser um membro de uma estrutura ou União, o destino de um ponteiro ou o tipo base de uma matriz.
-   Um tipo de dados declarado como um tipo de pipe só pode ser usado como um parâmetro de uma chamada remota.
-   Você pode passar um parâmetro de pipe em ambas as direções por valor ou por referência ( **\[** ponteiro [**ref**](ref.md) **\]** ). No entanto, não é possível aplicar o **\[** [](ptr.md) **\]** atributo PTR a um pipe que é passado por referência. Você não pode especificar um parâmetro de pipe com um **\[** [](unique.md) **\]** ponteiro exclusivo ou completo, independentemente da direção.
-   Você não pode usar pipes em interfaces de **\[** [**objeto**](object.md) **\]** .
-   Você não pode aplicar o **\[** [](idempotent.md) **\]** atributo idempotente a uma rotina que tem um parâmetro de pipe.
-   Você não pode usar os atributos de serialização, **\[** [**codificar**](encode.md) **\]** e **\[** [**decodificar**](decode.md) **\]** com pipes.
-   Você não pode usar identificadores automáticos, por padrão, ou com o **\[** atributo [**\_ identificador automático**](auto-handle.md) **\]** , com pipes.

> [!Note]  
> O compilador MIDL dá suporte somente a pipes no modo [**/OIF**](-oi.md) .

 

Para obter mais informações sobre como implementar rotinas com parâmetros de pipe, consulte [pipes](/windows/desktop/Rpc/pipes) no guia do programador de RPC e referência.

## <a name="examples"></a>Exemplos

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**RET**](decode.md)
</dt> <dt>

[**codificado**](encode.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**idempotente**](idempotent.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[**Marshal do usuário \_**](user-marshal.md)
</dt> <dt>

[**\_marshaling de transmissão**](wire-marshal.md)
</dt> </dl>

 

 