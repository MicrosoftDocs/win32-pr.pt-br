---
title: atributo defaultbind
description: O atributo \ defaultbind \ indica a propriedade única e vinculável que melhor representa o objeto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- atributo defaultbind MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a981d0469219a32b5931507f5df6d742e84fa67e6676e44c24edfb823f521a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807292"
---
# <a name="defaultbind-attribute"></a>atributo defaultbind

O atributo **\[ defaultbind \]** indica a propriedade única e vinculável que melhor representa o objeto.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à função. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função à qual o atributo **\[ defaultbind \]** será aplicado.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

As propriedades que têm o atributo **\[ defaultbind \]** também devem ter o **\[** atributo [**acoplável**](bindable.md) **\]** . Somente uma propriedade em uma interface ou dispinterface pode ter o atributo **\[ defaultbind \]** .

Esse atributo é usado por contêineres que têm um modelo de usuário envolvendo a associação a um objeto em vez de associar a uma propriedade de um objeto. Um objeto pode dar suporte à ligação de dados, mas não tem esse atributo.

### <a name="flags"></a>Flags

FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 