---
title: atributo noncreatable
description: O atributo \ noncreatable\ define um objeto que não pode ser instautado por si só.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- atributo nãocreatable MIDL
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59c53d8e4c05d15d55a6ccd9d7fb2b5cd8783463d1f59d439c74240fdd93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066936"
---
# <a name="noncreatable-attribute"></a>atributo noncreatable

O **\[ atributo nãocreatable \]** define um objeto que não pode ser instautado por si só.

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

Outros atributos que se aplicam à classe .

</dd> <dt>

*coclass-name* 
</dt> <dd>

O nome da classe.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Uma lista de interfaces para a classe .

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ noncreatable \]** em uma instrução [**coclass**](coclass.md) para indicar aos usuários que eles não podem criar um novo objeto dessa classe no nível superior, ou seja, chamando **CreateInstance** ou **CoCreateInstance**. A insta instação de um objeto dessa classe requer uma chamada de método para outro objeto. Por exemplo, Microsoft Excel, o objeto "Célula" não é recriável e deve ser obtido de um objeto Microsoft Excel Worksheet.

Métodos que retornam instâncias de classes não recriáveis devem retornar o tipo exato do objeto, em vez de **tipos VARIANT** ou **IDispatch.** \*

### <a name="typeflag-representation"></a>Representação de typeflag:

A ausência de TYPEFLAG \_ FCANCREATE.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 