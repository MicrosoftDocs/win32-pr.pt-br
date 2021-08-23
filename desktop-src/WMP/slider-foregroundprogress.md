---
title: SLIDER. foregroundProgress
description: O atributo foregroundProgress especifica ou recupera a posição atual da barra de progresso em primeiro plano como uma porcentagem da área do controle deslizante.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Controle deslizante. foregroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48819a2b3245fc8a72d29e9a30135cc37702417ca498c88b8be01578b74988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646336"
---
# <a name="sliderforegroundprogress"></a>SLIDER. foregroundProgress

O atributo **foregroundProgress** especifica ou recupera a posição atual da barra de progresso em primeiro plano como uma porcentagem da área do controle deslizante.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**float**) que varia de 0 a 100.

## <a name="remarks"></a>Comentários

Esse atributo é usado principalmente para acompanhar o progresso do download de um arquivo de mídia enquanto controla simultaneamente a posição de execução atual do arquivo usando o atributo **Value** . A posição da miniatura deslizante é restrita à área do andamento do primeiro plano. Isso permite que a busca interativa ocorra somente dentro da parte disponível de um arquivo de download.

Para usar essa funcionalidade, o atributo **useForegroundProgress** deve ser definido como true.

## <a name="examples"></a>Exemplos


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. min**](slider-min.md)
</dt> <dt>

[**SLIDER. Max**](slider-max.md)
</dt> <dt>

[**SLIDER. useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**Controle deslizante. valor**](slider-value.md)
</dt> </dl>

 

 





