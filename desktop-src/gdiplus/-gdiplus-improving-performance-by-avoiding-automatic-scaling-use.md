---
description: se você passar apenas o canto superior esquerdo de uma imagem para o método DrawImage, Windows GDI+ poderá dimensionar a imagem, o que diminuiria o desempenho.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Melhorando o desempenho, evitando o dimensionamento automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac74fbf636f3f1cbdf088939ad76732907c15228e66662a7246b3f0c0313c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778726"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Melhorando o desempenho, evitando o dimensionamento automático

se você passar apenas o canto superior esquerdo de uma imagem para o método **DrawImage** , Windows GDI+ poderá dimensionar a imagem, o que diminuiria o desempenho.

A chamada a seguir para o método **DrawImage** especifica um canto superior esquerdo de (50, 30), mas não especifica um retângulo de destino:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Embora essa seja a versão mais fácil do método **DrawImage** em termos do número de argumentos necessários, ela não é necessariamente a mais eficiente. se o número de pontos por polegada no dispositivo de vídeo atual for diferente do número de pontos por polegada no dispositivo em que a imagem foi criada, GDI+ dimensionará a imagem para que seu tamanho físico no dispositivo de vídeo atual seja o mais próximo possível de seu tamanho físico no dispositivo em que foi criado.

Se você quiser evitar esse dimensionamento, passe a largura e a altura de um retângulo de destino para o método **DrawImage** . O exemplo a seguir desenha a mesma imagem duas vezes. No primeiro caso, a largura e altura do retângulo de destino não são especificados, e a escala da imagem é ajustada automaticamente. No segundo caso, a largura e altura (medidas em pixels) do retângulo de destino são especificadas como iguais à largura e altura da imagem original.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



A ilustração a seguir mostra a imagem renderizada duas vezes.

![captura de tela de uma janela que contém duas versões de uma imagem em escalas diferentes](images/scaledtexture1.png)

 

 



