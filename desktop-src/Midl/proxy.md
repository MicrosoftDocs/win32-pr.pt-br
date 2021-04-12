---
title: atributo de proxy
description: O atributo \ proxy \ impede que a automação se registre como um manipulador de proxy/stub para uma interface dupla.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- atributo proxy MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453975"
---
# <a name="proxy-attribute"></a>atributo de proxy

O atributo **\[ proxy \]** impede que a automação se registre como um manipulador de proxy/stub para uma interface dupla.

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cadeia de caracteres-UUID* 
</dt> <dd>

Especifica uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen, em seguida, três grupos de quatro dígitos hexadecimais, cada um seguido por um hífen e 12 dígitos hexadecimais. Você pode colocar a cadeia de caracteres UUID entre aspas, exceto quando você usar o [**/OSF**](-osf.md)do compilador MIDL switch.

</dd> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Nome da interface.

</dd> <dt>

*interface base* 
</dt> <dd>

Especifica o nome de uma interface da qual essa interface derivada herda funções de membro, códigos de status e atributos de interface. A interface derivada não herda definições de tipo. Para fazer isso, use a palavra-chave [**Import**](import.md) para importar o arquivo IDL da interface base.

</dd> </dl>

## <a name="remarks"></a>Comentários

O uso do \[  \] atributo proxy para uma interface dupla impede que o tlb assuma os stubs gerados. Se esse atributo for especificado, o proxy de TypeLib não deverá ter o registro cancelado quando o registro de typelib tiver sido cancelado.

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG
</dt> <dd>

As interfaces podem ser marcadas com o \_ sinalizador de proxy TYPEFLAG para indicar que estarão usando uma biblioteca de vínculo dinâmico de proxy/stub. Esse sinalizador especifica que o proxy de TypeLib não deve ter o registro cancelado quando o typelib tem o registro cancelado.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gerando uma biblioteca de tipos com MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**simplifica**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 