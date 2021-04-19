---
title: Elemento AUTHOR
description: O elemento autor contém o nome do autor de um metarquivo de mídia do Windows ou clipe de mídia.
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
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784921"
---
# <a name="author-element"></a>Elemento AUTHOR

O elemento **autor** contém o nome do autor de um metarquivo de mídia do Windows ou clipe de mídia.

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

Esse elemento contém uma cadeia de texto que representa o nome do autor de um metarquivo de mídia do Windows ou clipe de mídia. Você pode usar o elemento **Author** dentro do elemento **ASX** e dentro de elementos de **entrada** .

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

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





