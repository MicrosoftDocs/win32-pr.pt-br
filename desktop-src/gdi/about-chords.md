---
description: Uma corda é uma região limitada pela interseção de uma elipse e um segmento de linha chamado de secante. A ilustração a seguir mostra uma corda desenhada usando a função de corda.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Sobre as cordas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502206"
---
# <a name="about-chords"></a>Sobre as cordas

Uma *corda* é uma região limitada pela interseção de uma elipse e um segmento de linha chamado de *secante*. A ilustração a seguir mostra uma corda desenhada usando a função de [**corda**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .

![ilustração de um elipse, mostrando dois radials, uma secante e uma corda](images/csfsh-02.png)

Ao chamar a [**corda**](/windows/win32/api/wingdi/nf-wingdi-chord), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse, bem como as coordenadas de dois pontos que definem dois radials. Um radial é uma linha desenhada do centro do retângulo delimitador de uma elipse para um ponto na elipse.

Quando o sistema desenha a parte curva da corda, ele faz isso usando a direção do arco atual para o contexto do dispositivo especificado. A direção do arco padrão é anti-horário. Você pode fazer com que seu aplicativo redefina a direção do arco chamando a função [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
