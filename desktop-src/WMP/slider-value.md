---
title: SLIDER.value
description: O atributo value especifica ou recupera a posição atual do controle deslizante. | SLIDER.value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- CONTROLE DESLIZANTE.value Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f9ae7c0dc45f3a14cad2aa5b7332b037302b6658043233bbd98b1d99a12e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118624"
---
# <a name="slidervalue"></a>SLIDER.value

O **atributo** value especifica ou recupera a posição atual do controle deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um  número de leitura/gravação (**float**) com um valor padrão **de min.**

## <a name="remarks"></a>Comentários

O **valor** sempre deve ser maior ou igual a **min** e menor ou igual a **máx.** Se você especificar um valor fora desse intervalo, **o valor** e a posição do controle deslizante não serão alterados.

Consulte **o DELIDER.** [atributo positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do **elemento SLIDER** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> </dl>

 

 





