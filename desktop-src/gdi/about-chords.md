---
description: Uma semente é uma região limitada pela interseção de uma elipse e um segmento de linha chamado selea. A ilustração a seguir mostra um cordão desenhado usando a função Demão.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Sobre os cordões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3bad0d17d34386ada7c7c3b46bb1bcc4db5f9a2ce572ce78c33f8f4b6af909
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400526"
---
# <a name="about-chords"></a>Sobre os cordões

Uma *semente* é uma região limitada pela interseção de uma elipse e um segmento de linha chamado *selea*. A ilustração a seguir mostra um cordão desenhado usando a [**função Demão.**](/windows/desktop/api/Wingdi/nf-wingdi-chord)

![ilustração de um elipse, mostrando dois radiais, uma sena e um cordão](images/csfsh-02.png)

Ao chamar [**o Recurso**](/windows/win32/api/wingdi/nf-wingdi-chord), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse, bem como as coordenadas de dois pontos que definem dois radiais. Um radial é uma linha desenhada do centro do retângulo delimitador de uma elipse para um ponto na elipse.

Quando o sistema desenha a parte curva do arco, ele faz isso usando a direção do arco atual para o contexto do dispositivo especificado. A direção padrão do arco é no sentido anti-horário. Você pode fazer com que seu aplicativo redefina a direção do arco chamando a [**função SetArcDirection.**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection)

 

 
