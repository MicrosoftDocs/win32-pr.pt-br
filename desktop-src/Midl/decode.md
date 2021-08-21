---
title: atributo decode
description: O atributo \ decode\ ACF especifica que um procedimento ou um tipo precisa de suporte à des serialização.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- decodificar atributo MIDL
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
# <a name="decode-attribute"></a>atributo decode

O **\[ atributo \]** ACF decodificar especifica que um procedimento ou um tipo precisa de suporte à des serialização.

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

*interface-attribute-list* 
</dt> <dd>

Especifica outros atributos que se aplicam à interface como um todo.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Especifica instruções IDL que formam a definição da interface.

</dd> <dt>

*op-attribute-list* 
</dt> <dd>

Especifica outros atributos operacionais que se aplicam ao procedimento, como **\[** [**codificar**](encode.md) **\]** .

</dd> <dt>

*proc-name* 
</dt> <dd>

Especifica o nome do procedimento.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica outros atributos, como **\[** [**codificar**](encode.md) **\]** e **\[** [**alocar**](allocate.md) **\]** .

</dd> <dt>

*type-name* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \] de decodificar** faz com que o compilador MIDL gere código que um aplicativo pode usar para recuperar dados serializados de um buffer. O **\[** [**atributo de**](encode.md) **\]** codificação dá suporte à serialização, gerando o código para serializar dados em um buffer.

Use os **\[** [**atributos de**](encode.md) **\]** **\[ \]** codificação e decodificar em um ACF para gerar código de serialização para procedimentos ou tipos definidos no arquivo IDL de uma interface. Quando usado como um atributo de interface, **\[ a \] decodificar** se aplica a todos os tipos e procedimentos definidos no arquivo IDL. Quando usado como um atributo de tipo, **\[ a \] decodificar** aplica-se somente ao tipo especificado. Quando usado como um atributo operacional, **\[ a decodificar \]** aplica-se somente a esse procedimento.

Para obter mais informações sobre como usar esse suporte de serialização, consulte [Serviços de Serialização e](/windows/desktop/Rpc/serialization-services) **\[** [**codificar**](encode.md) **\]** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Alocar**](allocate.md)
</dt> <dt>

[**Codificar**](encode.md)
</dt> </dl>

 

 