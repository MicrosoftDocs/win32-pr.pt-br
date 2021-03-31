---
title: atributo nonbrowsable
description: Use o atributo \ nonnavegável \ para marcar uma interface ou um membro de dispinterface que não deve ser exibido em um navegador de propriedades.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL de atributo não navegável
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917202"
---
# <a name="nonbrowsable-attribute"></a>atributo nonbrowsable

Use o atributo **\[ nonnavegável \]** para marcar uma interface ou um membro de dispinterface que não deve ser exibido em um navegador de propriedades.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade-atributo-lista* 
</dt> <dd>

Outros atributos que se aplicam à propriedade.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados retornados pelo método.

</dd> <dt>

*nome da propriedade* 
</dt> <dd>

O nome da propriedade ou do método.

</dd> <dt>

*prop-param-List* 
</dt> <dd>

Zero ou mais parâmetros a serem passados para o método.

</dd> </dl>

## <a name="remarks"></a>Comentários

Determinadas propriedades não devem ser exibidas em um navegador de propriedades. Isso pode ser porque a recuperação do valor levaria muito tempo. O exemplo impede que o usuário tente recuperar a propriedade *Count* , que retorna o número de linhas no dynaset. Esse número pode representar os resultados de uma consulta muito grande.

Outras propriedades podem ter efeitos inesperados no navegador. Por exemplo, considere um controle com a propriedade "IsSelected" para informar se o controle está selecionado. Se "IsSelected" for definido como false, um navegador de propriedades com base em seleção procurará um objeto diferente.

Observe que uma propriedade marcada como não **\[ navegável \]** ainda aparecerá em um pesquisador de objetos, que não mostra valores de propriedade.

### <a name="typeflag-representation"></a>Representação TYPEFLAG

A presença de FUNCFLAG \_ FNONBROWSABLE ou VARFLAG \_ FNONBROWSABLE.

## <a name="examples"></a>Exemplos

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 