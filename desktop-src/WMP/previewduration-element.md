---
title: Elemento PREVIEWDURATION
description: O elemento PREVIEWDURATION define o período de tempo que um clipe é reproduzido no modo de visualização.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Elemento PREVIEWDURATION do Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765240"
---
# <a name="previewduration-element"></a>Elemento PREVIEWDURATION

O elemento **PREVIEWDURATION** define o período de tempo que um clipe é reproduzido no modo de visualização.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obrigatório)

Período de tempo (em horas, minutos, segundos e centésimos de segundo) que o clipe reproduz no modo de visualização.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                    |
|-----------------|-----------------------------|
| Elementos pai | **ASX**, **entrada**, **referência** |
| Elementos filho  | Nenhum                        |



 

## <a name="remarks"></a>Comentários

Esse elemento define o período de tempo que um clipe é reproduzido no modo de visualização. Se esse elemento aparecer dentro de um elemento de **entrada** ou um elemento **ref** , ele se aplicará ao clipe definido por esse elemento. Se ele aparecer dentro do escopo de um elemento **ASX** , ele se aplicará a todos os clipes no metarquivo. Um elemento **PREVIEWDURATION** em um elemento **ref** tem precedência sobre um em um **elemento** de entrada e tem precedência sobre um elemento **PREVIEWDURATION** em um elemento **ASX** . Se nenhum elemento **PREVIEWDURATION** for definido para um clipe, o tempo de visualização padrão será de 10 segundos.

Se houver um elemento **StartTime** ou **STARTMARKER** para o clipe, o Windows Media Player renderizará o clipe começando no ponto definido por um desses elementos; caso contrário, ele será renderizado a partir do início do clipe. O clipe parará normalmente se for menor do que o tempo definido pelo elemento **PREVIEWDURATION** .

O elemento **Duration** substitui um elemento **PREVIEWDURATION** .

## <a name="examples"></a>Exemplos


```XML
<PREVIEWDURATION VALUE="0:30.0" />
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

 

 





