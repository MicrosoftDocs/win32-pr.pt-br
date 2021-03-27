---
description: Um retângulo é um polígono de quatro lados cujos lados opostos são paralelos e têm comprimento igual.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Retângulos de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827655"
---
# <a name="drawing-rectangles"></a>Retângulos de desenho

Um retângulo é um polígono de quatro lados cujos lados opostos são paralelos e têm comprimento igual. Embora um aplicativo possa desenhar um retângulo chamando a função [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , fornecendo as coordenadas de cada canto, a função [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) fornece um método mais simples. Essa função requer apenas as coordenadas dos cantos superior esquerdo e inferior direito. Quando um aplicativo chama a função [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , o sistema desenha o retângulo, excluindo os lados direito e inferior se nenhuma transformação do mundo for definida para o contexto do dispositivo fornecido.

Se uma transformação do mundo tiver sido definida usando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , o sistema incluirá as bordas direita e inferior.

Além de desenhar um retângulo tradicional, você pode desenhar retângulos com cantos arredondados. A função [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) requer que o aplicativo forneça as coordenadas dos cantos inferior esquerdo e superior direito, bem como a largura e a altura da elipse usada para arredondar cada canto.

Os aplicativos podem usar as seguintes funções para manipular retângulos.



| Função                         | Descrição                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | Redesenha o interior de um retângulo.                              |
| [**FrameRect**](/windows/desktop/api/Winuser/nf-winuser-framerect)   | Redesenha os lados de um retângulo.                                  |
| [**InvertRect**](/windows/desktop/api/Winuser/nf-winuser-invertrect) | Inverte as cores que aparecem dentro do interior de um retângulo. |



 

 

 
