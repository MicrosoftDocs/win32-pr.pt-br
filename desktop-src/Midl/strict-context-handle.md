---
title: strict_context_handle atributo
description: O atributo \ estrito \_ identificador de contexto \_ \ ACF define restrições em identificadores de contexto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle do atributo MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db19c74efa323fa7e3abc4bfd17c14a471cbb9c81414ae78064f84bfc19fa7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013574"
---
# <a name="strict_context_handle-attribute"></a>atributo de identificador de \_ contexto estrito \_

O atributo ACF do **\[ \_ \_ identificador \] de contexto estrito** define restrições em identificadores de contexto.

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Outros atributos de ACF que se aplicam à interface como um todo. Os atributos válidos [**incluem \_ identificador automático**](auto-handle.md), [**\_ identificador implícito**](implicit-handle.md), [**\_ identificador explícito**](explicit-handle.md)e [**otimizar**](optimize.md), [**código**](code.md)ou [**Nocode**](nocode.md). Separe vários atributos com vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

O nome da interface.

</dd> <dt>

*instruções de definição de interface* 
</dt> <dd>

Uma ou mais instruções MIDL que definem os elementos da [**interface**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Normalmente, quando uma chamada para um método de interface gera um identificador de contexto, esse identificador se torna livremente disponível para qualquer outra interface. Ao usar o atributo de **\[ \_ \_ identificador \] de contexto estrito** , você garante que os métodos nessa interface só aceitarão identificadores de contexto que foram criados por um método da mesma interface. Interfaces compiladas sem **\[ \_ \_ identificador \] de contexto estrito** não podem aceitar identificadores de contexto criados em interfaces compiladas com **\[ \_ \_ \] identificador de contexto estrito**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**auto-completar**](code.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_serializar identificador de contexto \_**](context-handle-serialize.md)
</dt> <dt>

[**identificador de contexto \_ \_ noserializeize**](context-handle-noserialize.md)
</dt> <dt>

[**\_identificador explícito**](explicit-handle.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**Nocode**](nocode.md)
</dt> <dt>

[**formato**](optimize.md)
</dt> <dt>

[tipo \_ de \_ identificador de contexto estrito \_](type-strict-context-handle.md)
</dt> </dl>

 

 