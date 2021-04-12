---
title: atributo uidefault
description: O atributo \ uidefault \ indica que o membro de informações de tipo é o membro padrão para exibição na interface do usuário.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault do atributo MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365868"
---
# <a name="uidefault-attribute"></a>atributo uidefault

O atributo **\[ uidefault \]** indica que o membro de informações de tipo é o membro padrão para exibição na interface do usuário.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de método* 
</dt> <dd>

Outros atributos que se aplicam ao método.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados que o método retornará quando concluir a execução.

</dd> <dt>

*nome do método* 
</dt> <dd>

O nome do método.

</dd> <dt>

*lista de parâmetros de método* 
</dt> <dd>

Zero ou mais parâmetros para o método.

</dd> </dl>

## <a name="remarks"></a>Comentários

Aplicar o atributo **\[ uidefault \]** a um membro de uma interface ou uma dispinterface informa Visual Basic, em tempo de design, para exibir automaticamente esse evento ou propriedade para o usuário. Isso significa que quando o usuário clica duas vezes em um objeto, Visual Basic salta para o evento na interface de origem padrão que tem o atributo **\[ uidefault \]** . Quando o usuário seleciona um objeto, Visual Basic navegador de Propriedades exibe a propriedade na interface de origem padrão que tem esse atributo. Se nenhum evento ou propriedade tiver o atributo **\[ uidefault \]** , Visual Basic exibirá o primeiro evento ou Propriedade listado na interface padrão.

### <a name="typeflag-representation"></a>Representação TYPEFLAG

A presença de FUNCFLAG \_ FUIDEFAULT ou VARFLAG \_ FUIDEFAULT

## <a name="examples"></a>Exemplos

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 