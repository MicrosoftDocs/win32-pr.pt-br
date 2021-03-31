---
title: atributo immediatebind
description: O atributo \ immediatebind \ indica que o banco de dados será notificado imediatamente de todas as alterações em uma propriedade de um objeto associado a um dado.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind do atributo MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161877"
---
# <a name="immediatebind-attribute"></a>atributo immediatebind

O atributo **\[ immediatebind \]** indica que o banco de dados será notificado imediatamente de todas as alterações a uma propriedade de um objeto associado a um dado.

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

*interface-atributo-lista* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Zero ou mais atributos de função.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ immediatebind \]** permite que os controles diferenciem as propriedades que precisam notificar o banco de dados de todas as alterações e as que não têm. Por exemplo, cada alteração em um controle de caixa de seleção deve ser enviada imediatamente ao banco de dados subjacente, mesmo que o controle não tenha perdido o foco. No entanto, para um controle ListBox, uma alteração ocorre sempre que uma seleção diferente é realçada. Notificar o banco de dados de uma alteração antes que o controle perca o foco seria ineficiente e desnecessário. O atributo **\[ immediatebind \]** permite que você especifique, definindo o bit immediatebind, as propriedades individuais em um formulário cujas alterações devem ser relatadas imediatamente.

As propriedades que têm o atributo **\[ immediatebind \]** também devem ter o **\[** atributo [**acoplável**](bindable.md) **\]** .

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

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 