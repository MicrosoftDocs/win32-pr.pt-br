---
title: atributo de decodificação
description: O atributo \ decodificar \ ACF especifica que um procedimento ou um tipo precisa de suporte de desserialização.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- atributo de decodificação MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30c70c821906bcfa4dedb8dbe87aab882866a4f21b7d561b16d3613f9041e0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384715"
---
# <a name="decode-attribute"></a>atributo de decodificação

O atributo **\[ decodificar \]** ACF especifica que um procedimento ou um tipo precisa de suporte de desserialização.

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica outros atributos que se aplicam à interface como um todo.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*interface-definição* 
</dt> <dd>

Especifica as instruções IDL que formam a definição da interface.

</dd> <dt>

*lista de atributos de op* 
</dt> <dd>

Especifica outros atributos operacionais que se aplicam ao procedimento, como **\[** [**Encode**](encode.md) **\]** .

</dd> <dt>

*proc-nome* 
</dt> <dd>

Especifica o nome do procedimento.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica outros atributos, como **\[** [**codificar**](encode.md) **\]** e **\[** [**alocar**](allocate.md) **\]** .

</dd> <dt>

*nome do tipo* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ decodificar \]** faz com que o compilador MIDL gere código que um aplicativo pode usar para recuperar dados serializados de um buffer. O **\[** [](encode.md) **\]** atributo codificar fornece suporte de serialização, gerando o código para serializar dados em um buffer.

Use os **\[** atributos de [**codificação**](encode.md) **\]** e **\[ decodificação \]** em um ACF para gerar código de SERIALIZAÇÃO para procedimentos ou tipos definidos no arquivo IDL de uma interface. Quando usado como um atributo de interface, **\[ decodificar \]** aplica-se a todos os tipos e procedimentos definidos no arquivo IDL. Quando usado como um atributo de tipo, **\[ decodificar \]** aplica-se somente ao tipo especificado. Quando usado como um atributo operacional, **\[ decodificar \]** aplica-se somente a esse procedimento.

Para obter mais informações sobre como usar esse suporte de serialização, consulte [serialização de serviços](/windows/desktop/Rpc/serialization-services) e **\[** [**codificação**](encode.md) **\]** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[**codificado**](encode.md)
</dt> </dl>

 

 