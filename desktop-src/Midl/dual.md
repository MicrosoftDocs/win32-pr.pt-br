---
title: atributo dual
description: O atributo Dual identifica uma interface que expõe propriedades e métodos por meio de IDispatch e diretamente por meio de VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL de atributo duplo
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917285"
---
# <a name="dual-attribute"></a>atributo dual

O atributo **Dual** identifica uma interface que expõe propriedades e métodos por meio de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e diretamente por meio de VTBL.

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a interface

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos MIDL adicionais.

</dd> <dt>

*nome da interface* 
</dt> <dd>

O nome da interface à qual o atributo **duplo** será aplicado.

</dd> </dl>

## <a name="remarks"></a>Comentários

As interfaces identificadas pelo atributo **Dual** devem ser compatíveis com a automação e ser derivadas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Este atributo não é permitido em dispinterfaces.

O atributo **Dual** cria uma interface que é uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e uma interface com (Component Object Model). As primeiras sete entradas do VTBL para uma interface dupla são os sete membros de **IDispatch**, e as entradas restantes são para o acesso direto aos membros da interface dupla. Todos os parâmetros e tipos de retorno especificados para membros de uma interface dupla devem ser tipos compatíveis com a automação.

Todos os membros de uma interface dupla devem passar um HRESULT como o valor de retorno da função. Membros, como funções de assessor de propriedade, que precisam retornar outros valores, devem especificar o último parâmetro como [**out**](out-idl.md), [**retval**](retval.md), indicando um parâmetro de saída que retorna o valor da função. Além disso, os membros que precisam dar suporte a várias localidades devem passar um parâmetro [**LCID**](lcid.md) .

Uma interface dupla fornece a velocidade da ligação VTBL direta e a flexibilidade da Associação de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Por esse motivo, as interfaces duplas são recomendadas sempre que possível.

> [!Note]  
> Se seu aplicativo acessa dados de objeto ao converter o *ponteiro dentro* da chamada de interface, você deve verificar os ponteiros de VTBL no objeto em relação aos seus próprios ponteiros do VTBL para garantir que você esteja conectado ao proxy apropriado.

 

A especificação de **Dual** em uma interface implica que a interface é compatível com a automação e, portanto, faz com que os \_ sinalizadores TYPEFLAG FDUAL e TYPEFLAG \_ FOLEAUTOMATION sejam definidos.

### <a name="flags"></a>Flags

TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 