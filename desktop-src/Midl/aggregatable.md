---
title: atributo agregável
description: O atributo \ agregável \ indica que a classe oferece suporte à agregação.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- MIDL de atributo agregável
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293962"
---
# <a name="aggregatable-attribute"></a>atributo agregável

O atributo **\[ agregável \]** indica que a classe oferece suporte à agregação.

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Categoria-atributo-lista* 
</dt> <dd>

Outros atributos que se aplicam à classe.

</dd> <dt>

*coclass-Name* 
</dt> <dd>

O nome da classe.

</dd> <dt>

*lista de interface de coclasse* 
</dt> <dd>

Uma lista de interfaces para a classe.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ agregável \]** em uma instrução [**coclass**](coclass.md) para permitir que os usuários saibam que a classe oferece suporte a agregações. Ou seja, a classe permite que suas interfaces sejam expostas por uma classe de contêiner como se essas interfaces fossem as próprias interfaces do contêiner.

A representação TYPEFLAG para esse atributo é TYPEFLAG \_ FAGGREGATABLE.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 