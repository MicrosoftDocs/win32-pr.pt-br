---
title: atributo nonbrowsable
description: Use o atributo \ nonbrowsable\ para marcar uma interface ou membro dispinterface que não deve ser exibido em um navegador de propriedades.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- atributo nonbrowsable MIDL
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6349683c3a3c591752036d9a5e2995d368460a049a79d2e1cf4123beb2b0ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066946"
---
# <a name="nonbrowsable-attribute"></a>atributo nonbrowsable

Use o **\[ atributo nonbrowsable \]** para marcar uma interface ou membro dispinterface que não deve ser exibido em um navegador de propriedades.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*property-attribute-list* 
</dt> <dd>

Outros atributos que se aplicam à propriedade .

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados retornados pelo método .

</dd> <dt>

*property-name* 
</dt> <dd>

O nome da propriedade ou método.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Zero ou mais parâmetros a serem passados para o método .

</dd> </dl>

## <a name="remarks"></a>Comentários

Determinadas propriedades não devem ser exibidas em um navegador de propriedades. Isso pode ocorrer porque a recuperação do valor levará muito tempo. O exemplo impede que o usuário tentar recuperar a *propriedade Count,* que retorna o número de linhas no dynaset. Esse número pode representar os resultados de uma consulta muito grande.

Outras propriedades podem ter efeitos inesperados no navegador. Por exemplo, considere um controle com a propriedade "IsSelected" para saber se o controle está selecionado. Se "IsSelected" for definido como false, um navegador de propriedades com base em seleção procurará um objeto diferente.

Observe que uma propriedade marcada como **\[ não nbrowsable \]** ainda aparecerá em um navegador de objetos, que não mostra valores de propriedade.

### <a name="typeflag-representation"></a>Representação de typeflag

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

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 