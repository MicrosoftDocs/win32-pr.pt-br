---
title: alterar atributo
description: A palavra-chave switch seleciona o discriminante para uma \_ União encapsulada.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- alterar atributo MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422b52a339a83cbaf59a9d65c0ed0e4e7e41533dcbf0be962147327145588a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013544"
---
# <a name="switch-attribute"></a>alterar atributo

A palavra-chave **switch** seleciona o discriminante para uma [**\_ União encapsulada**](encapsulated-unions.md).

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de opção* 
</dt> <dd>

Especifica um tipo [**int**](int.md), [**Char**](-char.md), [**enum**](enum.md) ou um identificador que resolve para um desses tipos.

</dd> <dt>

*nome do comutador* 
</dt> <dd>

Especifica o nome da variável do tipo *switch-type* que atua como o discriminante de União.

</dd> </dl>

## <a name="examples"></a>Exemplos

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Uniões não encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**switch \_ é**](switch-is.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**unida**](union.md)
</dt> </dl>

 

 




