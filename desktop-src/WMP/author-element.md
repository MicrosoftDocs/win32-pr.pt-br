---
title: Elemento AUTHOR
description: o elemento autor contém o nome do autor de um metarquivo de mídia Windows ou clipe de mídia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento de autor Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 058753d73049debe01e442f49bf12476642111549ad890e931100026badaeb3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098886"
---
# <a name="author-element"></a>Elemento AUTHOR

o elemento **autor** contém o nome do autor de um metarquivo de mídia Windows ou clipe de mídia.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento            |
|-----------------|--------------------|
| Elementos pai | **ASX**, **entrada** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

esse elemento contém uma cadeia de texto que representa o nome do autor de um metarquivo de mídia Windows ou clipe de mídia. Você pode usar o elemento **Author** dentro do elemento **ASX** e dentro de elementos de **entrada** .

Se esse elemento aparecer no elemento **ASX** , o texto será exibido como **Mostrar** informações.

Se esse elemento aparecer em um elemento de **entrada** , o texto será exibido como o autor do clipe.

Cada elemento de **entrada** e **ASX** pai deve conter no máximo um elemento de **autor** filho. Vários elementos de **autor** após o primeiro serão ignorados e não serão exibidos.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metarquivo de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





