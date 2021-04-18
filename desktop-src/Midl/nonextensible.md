---
title: atributo não extensível
description: O atributo \ extensível \ especifica que a implementação de IDispatch inclui apenas as propriedades e os métodos listados na descrição da interface e não pode ser estendido com membros adicionais em tempo de execução.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- MIDL de atributo não extensível
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752059"
---
# <a name="nonextensible-attribute"></a>atributo não extensível

O atributo **extensível \[ \]** especifica que a implementação de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) inclui apenas as propriedades e os métodos listados na descrição da interface e não pode ser estendido com membros adicionais em tempo de execução. (Por padrão, a automação pressupõe que as interfaces podem adicionar membros em tempo de execução; ou seja, elas pressupõem que são extensíveis.)

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**interface**](interface.md).

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos de interface MIDL.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*interface-definição* 
</dt> <dd>

Especifica as instruções IDL que formam a definição da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode aplicar o atributo **\[ extensível \]** a uma interface ou uma dispinterface. No entanto, uma interface também deve ter os **\[** atributos [**Dual**](dual.md) **\]** e **\[** [**oleautomation**](oleautomation.md) **\]** .

### <a name="flags"></a>Flags

TYPEFLAG \_ FNONEXTENSIBLE

## <a name="examples"></a>Exemplos

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Conteúdo de uma biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**simplifica**](dual.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 