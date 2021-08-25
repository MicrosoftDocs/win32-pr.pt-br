---
title: Criando controles deslizantes personalizados
description: Criando controles deslizantes personalizados
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Criando capas, controles deslizantes
- Windows Media Player capas, controles deslizantes
- capas, controles deslizantes
- controles deslizantes em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85a789bbd90003b59e1a9b9dcf8fffcf4a126c38138f7a051c24125780f8c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902326"
---
# <a name="creating-custom-sliders"></a>Criando controles deslizantes personalizados

Você pode criar controles deslizantes personalizados em qualquer forma desejada. Neste exemplo, uma faixa simples é escolhida, mas a forma real pode ser qualquer coisa. Este é o código para o elemento **CUSTOMSLIDER** :


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



Isso configura um valor inicial para o controle deslizante. Dois novos bitmaps são introduzidos. Um é o bitmap em escala de cinza (slider.bmp) que define quais valores serão usados quando clicados e o outro (slider.bmp) que determina qual imagem será mostrada quando uma parte específica da escala de cinza for clicada.

O valor inicial é determinado pela escuta do volume com wmpprop e, em seguida, o volume pode ser alterado quando o usuário clica em uma parte do controle deslizante que dispara uma alteração no valor.

Você pode ver uma aparência de controle deslizante de trabalho semelhante na seção de exemplo do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de criação de capa**](skin-creation-guide.md)
</dt> </dl>

 

 




