---
title: Criando controles deslizantes personalizados
description: Criando controles deslizantes personalizados
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Criando capas, controles deslizantes
- Capas, controles deslizantes do Windows Media Player
- capas, controles deslizantes
- controles deslizantes em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498752"
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

 

 




