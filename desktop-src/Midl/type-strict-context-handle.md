---
title: type_strict_context_handle atributo
description: Use o identificador de \_ contexto estrito \ Type \_ \_ \ em um arquivo ACF para definir restrições em identificadores de contexto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle do atributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453983"
---
# <a name="type_strict_context_handle-attribute"></a>tipo \_ de \_ atributo de identificador de contexto estrito \_

Use o **\[ \_ \_ \_ identificador \] de contexto estrito de tipo** em um arquivo ACF para definir restrições em identificadores de contexto.

``` syntax
[ 
    type_strict_context_handle 
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

Para usar esse atributo, o sinalizador-Target deve ser definido como NT60 (ou superior) durante a execução de midl.exe.

\[tipo \_ \_ \_ de identificador de contexto estrito \] é um superconjunto funcional de \[ identificador de \_ contexto estrito \_ \] . No \[ \_ \_ identificador de contexto estrito \] , a ID de tipo do identificador é sempre 0; no \[ identificador de contexto de tipo \_ estrito \_ \_ \] , uma ID de tipo exclusivo é atribuída pelo compilador MIDL.

É recomendável usar o \[ \_ \_ \_ identificador de contexto de tipo estrito \] em vez do \[ identificador de \_ contexto estrito \_ \] . Os identificadores de contexto não são associados a um tipo específico por padrão. Quando vários tipos de identificadores de contexto são usados no mesmo processo, é possível que um cliente mal-intencionado passe um identificador de contexto em vez de outro para produzir resultados indesejáveis. O uso do \[ identificador de contexto de tipo \_ estrito \_ \_ \] permite que os aplicativos imponham a consistência de tipo de identificador de contexto e evitem qualquer uso de tipo de identificador de contexto incompatível.

Um identificador de contexto atribuído com o \[ identificador de contexto de tipo \_ estrito \_ \_ \] também não pode ser atribuído com um \[ identificador de \_ contexto estrito \_ \] .

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

[\_identificador de contexto estrito \_](strict-context-handle.md)
</dt> </dl>

 

 