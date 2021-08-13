---
title: atributo dual
description: O atributo duplo identifica uma interface que expõe propriedades e métodos por meio de IDispatch e diretamente por meio do VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- atributo duplo MIDL
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e1e9cd15c1b219d07518c9630880a5010226c96c63d57539ffb66fab3a6c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643090"
---
# <a name="dual-attribute"></a>atributo dual

O **atributo** duplo identifica uma interface que expõe propriedades e métodos por meio de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e diretamente por meio do VTBL.

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

*uuid-number* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a interface

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos MIDL adicionais.

</dd> <dt>

*interface-name* 
</dt> <dd>

O nome da interface à qual o **atributo** duplo será aplicado.

</dd> </dl>

## <a name="remarks"></a>Comentários

As interfaces identificadas pelo **atributo duplo** devem ser compatíveis com a Automação e ser derivadas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Esse atributo não é permitido em dispinterfaces.

O **atributo** duplo cria uma interface que é uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e uma interface COMPONENT OBJECT MODEL (COM). As primeiras sete entradas do VTBL para uma interface dupla são os sete membros de **IDispatch** e as entradas restantes são para acesso direto aos membros da interface dupla. Todos os parâmetros e tipos de retorno especificados para membros de uma interface dupla devem ser tipos compatíveis com Automação.

Todos os membros de uma interface dupla devem passar um HRESULT como o valor de retorno da função. Membros, como funções de acessador de propriedade, que precisam retornar outros valores, devem especificar o último parâmetro como [**out**](out-idl.md), [**retval**](retval.md), indicando um parâmetro de saída que retorna o valor da função. Além disso, os membros que precisam dar suporte a várias localidades devem passar um [**parâmetro lcid.**](lcid.md)

Uma interface dupla fornece a velocidade da associação VTBL direta e a flexibilidade da associação [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Por esse motivo, interfaces duplas são recomendadas sempre que possível.

> [!Note]  
> Se o aplicativo acessar dados  de objeto ao lançar o ponteiro this dentro da chamada de interface, você deverá verificar os ponteiros VTBL no objeto em relação aos seus próprios ponteiros VTBL para garantir que você esteja conectado ao proxy apropriado.

 

Especificar **duplo em** uma interface implica que a interface é compatível com a Automação e, portanto, faz com que os sinalizadores \_ TYPEFLAG FDUAL e TYPEFLAG FOL \_ DIGITTOMATION sejam definidos.

### <a name="flags"></a>Flags

TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOL DIGITOTOMATION

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

[**Interface**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 