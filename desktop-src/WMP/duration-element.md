---
title: Elemento DURATION
description: O elemento DURATION define o período de tempo durante o qual o Windows Media Player processará a entrada da playlist associada.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION do Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796433"
---
# <a name="duration-element"></a>Elemento DURATION

O elemento **Duration** define o período de tempo durante o qual o Windows Media Player processará a entrada da playlist associada.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obrigatório)

O período de tempo, em horas, minutos, segundos e centésimos de segundo, que uma entrada é renderizada pelo Windows Media Player. O valor padrão é o comprimento total da entrada. Se a entrada for um arquivo gráfico, um valor de duração deverá ser especificado.

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

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





