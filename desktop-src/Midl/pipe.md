---
title: atributo pipe
description: O construtor de tipo de pipe possibilita transmitir um fluxo aberto de dados digitados em uma chamada de procedimento remoto.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- atributo pipe MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c407bef0a9e610d21e7221eb9a06560f33300f4f1f388fa699ca9dfb18531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641949"
---
# <a name="pipe-attribute"></a>atributo pipe

O **construtor** de tipo de pipe possibilita transmitir um fluxo aberto de dados digitados em uma chamada de procedimento remoto.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de elemento* 
</dt> <dd>

Define o tamanho de um único elemento no buffer de transferência. O *tipo de elemento* pode ser um tipo [base,](midl-base-types.md)tipo \_ predefinido, [**struct**](struct.md), [**enum de 32b**](v1-enum.md)ou identificador de tipo. Várias restrições se aplicam *aos \_ tipos de* elemento , conforme descrito em Comentários, abaixo.

</dd> <dt>

*pipe-declarator* 
</dt> <dd>

Especifica um ou mais identificadores ou ponteiros para identificadores. Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar o construtor **de** tipo de pipe para transmitir dados em ambas as direções. Um parâmetro no pipe permite que o servidor e pull do fluxo **\[** [](in.md) **\]** de dados do cliente durante uma chamada de procedimento remoto. Um **\[** [**parâmetro de**](out-idl.md) **\]** pipe out permite que o servidor es por push o fluxo de dados de volta para o cliente. Você fornece as rotinas do lado do cliente para push e pull do fluxo de dados e para alocar um buffer global para os dados. As rotinas de stub de cliente e servidor empacotam e unmarshal dados e passam uma referência ao buffer de volta para o aplicativo.

As seguintes restrições se aplicam a pipes:

-   Um elemento pipe não pode ser ou conter um ponteiro, uma matriz compatível ou variável, um handle ou um alça de contexto. Além disso, na implementação da Microsoft de pipes, um elemento pipe não pode ser ou conter uma união [**,**](union.md)uma [**enum de 16b**](enum.md)ou [**\_ \_ um int3264**](--int3264.md).
-   Você não pode aplicar a **\[** [**transmissão \_ como**](transmit-as.md) **\]** , representar **\[** [**\_ como**](represent-as.md) **\]** , marshal **\[** [**\_**](wire-marshal.md) **\]** **\[** [**\_**](user-marshal.md) **\]** de transmissão ou atributos de marshal de usuário a um tipo de pipe ou ao tipo de elemento .
-   Um tipo de pipe não pode ser membro de uma estrutura ou união, o destino de um ponteiro ou o tipo base de uma matriz.
-   Um tipo de dados declarado como um tipo de pipe só pode ser usado como um parâmetro de uma chamada remota.
-   Você pode passar um parâmetro de pipe em qualquer direção por valor ou por referência **\[** [**(ponteiro ref).**](ref.md) **\]** No entanto, você não pode **\[** [**aplicar o atributo ptr**](ptr.md) **\]** a um pipe que é passado por referência. Não é possível especificar um parâmetro de pipe com um ponteiro **\[** [](unique.md) **\]** exclusivo ou completo, independentemente da direção.
-   Não é possível usar pipes em **\[** [](object.md) **\]** interfaces de objeto.
-   Não é possível aplicar **\[** [**o atributo idempotente**](idempotent.md) **\]** a uma rotina que tenha um parâmetro de pipe.
-   Você não pode usar os atributos de serialização, **\[** [**codificar**](encode.md) **\]** e **\[** [**decodificar**](decode.md) com **\]** pipes.
-   Você não pode usar alças automáticas, por padrão, ou com o atributo **\[** [**de \_ alça**](auto-handle.md) **\]** automática, com pipes.

> [!Note]  
> O compilador MIDL dá suporte apenas a pipes [**no modo /Oif.**](-oi.md)

 

Para obter mais informações sobre como implementar rotinas com parâmetros de pipe, consulte [Pipes](/windows/desktop/Rpc/pipes) no Guia e referência do programador RPC.

## <a name="examples"></a>Exemplos

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**auto \_ handle**](auto-handle.md)
</dt> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**Decodificar**](decode.md)
</dt> <dt>

[**Codificar**](encode.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**idempotente**](idempotent.md)
</dt> <dt>

[**Em**](in.md)
</dt> <dt>

[**Objeto**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**marshal \_ de usuário**](user-marshal.md)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> </dl>

 

 