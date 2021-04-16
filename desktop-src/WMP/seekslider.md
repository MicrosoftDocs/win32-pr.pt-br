---
title: SEEKSLIDER
description: Este é um controle deslizante predefinido com os valores padrão a seguir. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747286"
---
# <a name="seekslider"></a>SEEKSLIDER

Este é um **controle deslizante** predefinido com os valores padrão a seguir.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Comentários

Isso cria um controle **deslizante** que procura o arquivo de mídia em qualquer posição. As dicas de ferramenta são localizadas. Todas as propriedades desse **controle deslizante** podem ser substituídas especificando-as explicitamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 





