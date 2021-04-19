---
title: Elemento endmarcer
description: O elemento endmarcer especifica um marcador no qual o Windows Media Player irá parar de renderizar o fluxo.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Elemento de marca de fim do Windows Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811109"
---
# <a name="endmarker-element"></a>Elemento endmarcer

O elemento **ENDmarcer** especifica um marcador no qual o Windows Media Player irá parar de renderizar o fluxo.

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Atributos

**AUTOMÁTICA**

O número de um marcador numérico no índice. O valor padrão é o final do conteúdo.

**NOME**

O nome de um marcador nomeado no índice. O valor padrão é o final do conteúdo.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **entrada**, **ref** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento Especifica o marcador em que o Windows Media Player deve parar de renderizar o fluxo definido na **entrada** pai ou no elemento **ref** .

Observação

Use o elemento **ENDmarcer** com o atributo **Number** ou **Name** , mas não ambos.

No modo de visualização, atingir um marcador final interrompe a visualização, mesmo que o tempo especificado pelo elemento **PREVIEWDURATION** não tenha decorrido. O elemento **ENDmarcer** também tem precedência sobre o elemento **Duration** .

Um elemento de **marca de fim** definido em um elemento **ref** tem PREcedência sobre um **marca de fim** definido dentro do elemento de **entrada** pai do elemento **ref** .

Se o marcador especificado por um elemento de **marca de fim** ocorrer anteriormente no fluxo do que o marcador definido por um elemento **STARTMARKER** , nenhum conteúdo será reproduzido, mas nenhum erro é gerado.

## <a name="examples"></a>Exemplos


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





