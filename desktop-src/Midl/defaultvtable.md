---
title: atributo defaultvtable
description: O atributo \ defaultvtable \ define uma interface como a interface padrão vtable.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- MIDL de atributo defaultvtable
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffebc5907072f7fdfc539bbc2b06bf1e4ad9fb667826c6c3c5a96121b106326e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067336"
---
# <a name="defaultvtable-attribute"></a>atributo defaultvtable

O atributo **\[ defaultvtable \]** define uma interface como a interface padrão vtable.

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
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

Outros atributos que se aplicam à classe. Os **\[** atributos de [**origem**](source.md) **\]** e **\[** [**UUID**](uuid.md) **\]** são necessários.

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

Uma interface vtable padrão não pode ser um dispinterface — ela deve ser uma interface dupla ou vtable. Se a interface for uma interface dupla, os coletores poderão assumir que receberão eventos por meio de vtable.

Uma classe pode ser uma interface de origem padrão e uma interface de origem vtable padrão, conforme mostrado no exemplo. Nesse caso, um coletor de aviso deve usar IID \_ IDISPATCH para receber eventos de expedição e usar o identificador de interface para receber eventos vtable.

### <a name="typeflag-representation"></a>Representação TYPEFLAG

A presença de IMPLTYPEFLAG \_ FDEFAULTVTABLE.

## <a name="examples"></a>Exemplos

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
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
</dt> <dt>

[**original**](source.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> </dl>

 

 