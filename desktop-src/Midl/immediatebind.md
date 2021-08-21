---
title: atributo immediatebind
description: O atributo \ immediatebind\ indica que o banco de dados será notificado imediatamente de todas as alterações em uma propriedade de um objeto vinculado a dados.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- atributo immediatebind MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40396343177da07a2747c79473cdc52f2d665fea8411f4d6f117a5032d66707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642972"
---
# <a name="immediatebind-attribute"></a>atributo immediatebind

O **\[ atributo \] immediatebind** indica que o banco de dados será notificado imediatamente de todas as alterações em uma propriedade de um objeto vinculado a dados.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica o nome da [**interface ou**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Zero ou mais atributos de função.

</dd> <dt>

*Returntype* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \] immediatebind** permite que os controles diferenciem entre as propriedades que precisam notificar o banco de dados de cada alteração e aquelas que não fazem isso. Por exemplo, todas as alterações em um controle de caixa de seleção devem ser enviadas imediatamente para o banco de dados subjacente, mesmo que o controle não tenha perdido o foco. No entanto, para um controle de caixa de listagem, uma alteração ocorre sempre que uma seleção diferente é realçada. Notificar o banco de dados de uma alteração antes que o controle perca o foco seria ineficiente e desnecessário. O **\[ atributo \] immediatebind** permite que você especifique, definindo o bit ImmediateBind, propriedades individuais em um formulário cujas alterações devem ser relatadas imediatamente.

As propriedades que têm **\[ o atributo \] immediatebind** também devem ter o atributo a **\[** [**vinciável.**](bindable.md) **\]**

### <a name="flags"></a>Flags

FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 