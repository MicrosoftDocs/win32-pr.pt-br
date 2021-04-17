---
title: Elemento TITLE (metarquivo)
description: O elemento TITLE define uma cadeia de texto especificando o título de um elemento ASX ou de entrada.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento de título (metarquivo) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811682"
---
# <a name="title-element-metafile"></a>Elemento TITLE (metarquivo)

O elemento **title** define uma cadeia de texto especificando o título de um elemento **ASX** ou de **entrada** .

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **ASX**, **entrada** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento define uma cadeia de texto que especifica o título de um elemento **ASX** ou de **entrada** . O título é exibido na caixa de diálogo painel de exibição e **Propriedades** .

Quando esse elemento aparece dentro de um elemento **ASX** , o texto é exibido como **Mostrar** informações. Quando esse elemento aparece dentro de um elemento de **entrada** , o texto é exibido como informações de **clipe** .

Se um elemento **moreinfo** também for usado com o elemento associado (pai), será o texto do título no qual o usuário clica para acessar a URL definida no elemento **moreinfo** .

Cada elemento de **entrada** e **ASX** pai deve conter no máximo um elemento de **título** filho. Vários elementos **title** após o primeiro serão ignorados e não serão exibidos.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





