---
title: Elemento DURATION
description: o elemento DURATION define o período de tempo Windows Media Player processará a entrada da playlist associada.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b06b497a6d31b03c4cbec23748f6995a1382fb806ad18fabaa542ed8ff33e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863346"
---
# <a name="duration-element"></a>Elemento DURATION

o elemento **DURATION** define o período de tempo Windows Media Player processará a entrada da playlist associada.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obrigatório)

O período de tempo, em horas, minutos, segundos e centésimos de um segundo, que uma entrada é renderizada pelo Windows Media Player. O valor padrão é o comprimento total da entrada. Se a entrada for um arquivo gráfico, um valor de duração deverá ser especificado.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **entrada**, **ref** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento define o período de tempo que um fluxo deve ser renderizado. Se o atributo de **valor** exceder o comprimento do fluxo de conteúdo, o fluxo será encerrado em seu ponto de extremidade normal.

Esse elemento pode aparecer em um elemento **ref** ou dentro de um elemento **entry** . No entanto, um elemento **Duration** definido dentro de um elemento **ref** substitui um que aparece dentro do elemento de **entrada** pai do elemento **ref** .

O elemento **Duration** substitui um elemento **PREVIEWDURATION** .

## <a name="examples"></a>Exemplos


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metarquivo de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





