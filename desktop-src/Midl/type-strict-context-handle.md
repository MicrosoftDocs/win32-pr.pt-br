---
title: type_strict_context_handle atributo
description: Use \type \_ strict \_ context \_ handle\ em um arquivo ACF para definir restrições em identificador de contexto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle atributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e10c6231ac41287a08df7b9a0fa4e5361eddec9eb72bb6059b9f00dea5106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105616"
---
# <a name="type_strict_context_handle-attribute"></a>atributo de \_ \_ identificador de \_ contexto estrito de tipo

Use o **\[ \_ identificador de \_ contexto \_ estrito de \]** tipo em um arquivo ACF para definir restrições em identificador de contexto.

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

*interface-attribute-list* 
</dt> <dd>

Outros atributos do ACF que se aplicam à interface como um todo. Os atributos válidos incluem o manipular [**\_ automaticamente**](auto-handle.md), [**o \_ alça**](implicit-handle.md)implícito, [**o \_ handle**](explicit-handle.md)explícito [**e otimizar**](optimize.md)o , o [**código**](code.md)ou [**o nocode**](nocode.md). Separe vários atributos com vírgulas.

</dd> <dt>

*interface-name* 
</dt> <dd>

O nome da interface.

</dd> <dt>

*interface-definition-statements* 
</dt> <dd>

Uma ou mais instruções MIDL que definem os elementos da [**interface**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar esse atributo, o sinalizador -target deve ser definido como NT60 (ou superior) ao executar midl.exe.

\[O \_ \_ identificador de \_ contexto estrito \] de tipo é um superconjunto funcional do \[ \_ identificador de contexto \_ estrito \] . No identificador de contexto estrito , a ID de tipo do identificador é sempre 0; no identificador de contexto estrito do tipo , uma ID de tipo exclusiva é atribuída pelo \[ \_ \_ \] \[ \_ \_ \_ \] compilador MIDL.

É recomendável usar o identificador de \[ \_ contexto \_ \_ estrito de tipo em vez do \] \[ \_ identificador de contexto \_ estrito \] . Identificador de contexto não estão associados a um tipo específico por padrão. Quando vários tipos de alças de contexto são usados no mesmo processo, é possível que um cliente mal-intencionado passe um handle de contexto no lugar de outro para produzir resultados indesejáveis. O uso do identificador de contexto estrito de tipo permite que os aplicativos imigram a consistência do tipo de identificador de contexto e impeçam qualquer uso de tipo de identificador de contexto \[ \_ \_ \_ \] incompatibilidade.

Um identificador de contexto atribuído com o \[ identificador \_ de contexto \_ \_ estrito de tipo também não pode \] ser atribuído com o \[ \_ identificador de contexto \_ estrito \] .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Código**](code.md)
</dt> <dt>

[Alças de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**serializar \_ o \_ alça de contexto**](context-handle-serialize.md)
</dt> <dt>

[**\_ \_ naerialize do context handle**](context-handle-noserialize.md)
</dt> <dt>

[**alça \_ explícita**](explicit-handle.md)
</dt> <dt>

[**alça \_ implícita**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Otimizar**](optimize.md)
</dt> <dt>

[strict \_ context \_ handle](strict-context-handle.md)
</dt> </dl>

 

 