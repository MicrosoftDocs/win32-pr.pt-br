---
title: Elemento TITLE (metafile)
description: O elemento TITLE define uma cadeia de caracteres de texto que especifica o título para um elemento ASX ou ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (metafile) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 085bec9a9937c8dbd02fad6df785f4bce7afea90a74117e745f09cb5135633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117716"
---
# <a name="title-element-metafile"></a>Elemento TITLE (metafile)

O **elemento TITLE** define uma cadeia de caracteres de texto que especifica o título para um elemento **ASX** **ou ENTRY.**

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
| Elementos pai | **ASX**, **ENTRY** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento define uma cadeia de caracteres de texto que especifica o título de um **elemento ASX** **ou ENTRY.** O título é exibido no painel de exibição e na **caixa de diálogo** Propriedades.

Quando esse elemento aparece em um **elemento ASX,** o texto é exibido como **Mostrar** informações. Quando esse elemento aparece dentro de **um elemento ENTRY,** o texto é exibido como Informações **de** clipe.

Se um **elemento MOREINFO** também for usado com o elemento associado (pai), será o texto do título que o usuário clica para acessar a URL definida no **elemento MOREINFO.**

Cada elemento **PAI ASX** e **ENTRY** deve conter no máximo um elemento **TITLE** filho. Vários **elementos TITLE** após o primeiro serão ignorados e não serão exibidos.

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

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





