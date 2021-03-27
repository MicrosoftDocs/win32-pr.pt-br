---
description: O sistema de coordenadas de uma janela é baseado no sistema de coordenadas do dispositivo de vídeo.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Sistema de coordenadas da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661964"
---
# <a name="window-coordinate-system"></a>Sistema de coordenadas da janela

O sistema de coordenadas de uma janela é baseado no sistema de coordenadas do dispositivo de vídeo. A unidade básica de medida é a unidade do dispositivo (normalmente, o pixel). Os pontos na tela são descritos por pares de coordenadas x e y. As coordenadas x aumentam para a direita; as coordenadas y aumentam de cima para baixo. A origem (0, 0) para o sistema depende do tipo de coordenadas que está sendo usado.

O sistema e os aplicativos especificam a posição de uma janela na tela em *coordenadas da tela*. Para coordenadas de tela, a origem é o canto superior esquerdo da tela. A posição completa de uma janela é geralmente descrita por uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas de tela de dois pontos que definem os cantos superior esquerdo e inferior direito da janela.

O sistema e os aplicativos especificam a posição de pontos em uma janela usando as *coordenadas do cliente*. A origem, nesse caso, é o canto superior esquerdo da área da janela ou do cliente. As coordenadas do cliente garantem que um aplicativo possa usar valores de coordenadas consistentes ao desenhar na janela, independentemente da posição da janela na tela.

As dimensões da área do cliente também são descritas por uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas do cliente para a área. Em todos os casos, a coordenada superior esquerda do retângulo é incluída na janela ou na área do cliente, enquanto a coordenada inferior direita é excluída. As operações gráficas em uma área de janela ou cliente são excluídas das bordas direita e inferior do retângulo delimitador.

Ocasionalmente, os aplicativos podem ser necessários para mapear as coordenadas em uma janela para as de outra janela. Um aplicativo pode mapear coordenadas usando a função [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) . Se uma das janelas for a janela da área de trabalho, a função efetivamente converterá coordenadas de tela em coordenadas de cliente e vice-versa; a janela da área de trabalho é sempre especificada em coordenadas da tela.

 

 
