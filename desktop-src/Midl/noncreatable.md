---
title: atributo noncreatable
description: O atributo \ não define um objeto que não pode ser instanciado por si só.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL de atributo não-cri
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293951"
---
# <a name="noncreatable-attribute"></a>atributo noncreatable

O atributo não- **\[ cri \]** define um objeto que não pode ser instanciado por si só.

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

Use o **\[ \] atributo não** criável em uma instrução [**coclass**](coclass.md) para indicar aos usuários que eles não podem criar um novo objeto dessa classe no nível superior — ou seja, chamando **CreateInstance** ou **CoCreateInstance**. A instanciação de um objeto dessa classe requer uma chamada de método para outro objeto. Por exemplo, no Microsoft Excel, o objeto "Cell" não pode ser acessado e deve ser obtido de um objeto planilha do Microsoft Excel.

Os métodos que retornam instâncias de classes não-retornáveis devem retornar o tipo exato do objeto, em vez de tipos **Variant** ou **IDispatch** \* .

### <a name="typeflag-representation"></a>Representação de TYPEFLAG:

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

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 