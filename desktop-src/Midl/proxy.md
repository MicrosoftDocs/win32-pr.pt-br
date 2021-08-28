---
title: atributo proxy
description: O atributo \ proxy\ impede que a Automação se registre como um manipulador de proxy/stub para uma interface dupla.
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
ms.openlocfilehash: 37e81cb7f67f87153825db59d921b6ee9ec7df6cd334ed2228896c8dec5f9d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641414"
---
# <a name="proxy-attribute"></a>atributo proxy

O **\[ atributo proxy \]** impede que a Automação se registre como um manipulador de proxy/stub para uma interface dupla.

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

*string-uuid* 
</dt> <dd>

Especifica uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen e, em seguida, três grupos de quatro dígitos hexadecimais, cada um seguido por um hífen e, em seguida, 12 dígitos hexadecimais. Você pode colocar a cadeia de caracteres UUID entre aspas, exceto quando usar a opção do compilador MIDL [**/osf**](-osf.md).

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome da interface.

</dd> <dt>

*interface base* 
</dt> <dd>

Especifica o nome de uma interface da qual essa interface derivada herda funções de membro, códigos de status e atributos de interface. A interface derivada não herda definições de tipo. Para fazer isso, use a [**palavra-chave import**](import.md) para importar o arquivo IDL da interface base.

</dd> </dl>

## <a name="remarks"></a>Comentários

Usar o \[ **atributo proxy** \] para uma interface dupla impede que o TLB assumindo stubs gerados. Se esse atributo for especificado, o proxy typelib não deverá ter o registro não feito quando o typelib não tiver o registro.

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG \_ PROXY
</dt> <dd>

As interfaces podem ser marcadas com o sinalizador PROXY TYPEFLAG para indicar que usarão uma biblioteca de link dinâmico \_ proxy/stub. Esse sinalizador especifica que o proxy typelib não deve ter o registro não feito quando o typelib não for feito o registro.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gerando uma biblioteca de tipos com MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Dupla**](dual.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 