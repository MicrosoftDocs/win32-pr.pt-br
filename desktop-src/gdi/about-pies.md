---
description: Uma pizza é uma região limitada pela interseção de uma curva de elipse e dois radiais. A ilustração a seguir mostra uma pizza desenhada usando a função Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Sobre pizzas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e447e313a3088bbf9a72c790115fb3bb25770017cf13ce7922685fd18ccfe671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966456"
---
# <a name="about-pies"></a>Sobre pizzas

Uma *pizza* é uma região limitada pela interseção de uma curva de elipse e dois radiais. A ilustração a seguir mostra uma pizza desenhada usando a [**função Pie.**](/windows/desktop/api/Wingdi/nf-wingdi-pie)

![ilustração mostrando uma elipse com uma pizza sombreada](images/csfsh-03.png)

Ao chamar [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse, bem como as coordenadas de dois pontos que definem dois radiais.

Quando o sistema desenha a parte curva da pizza, ele usa a direção do arco atual para o contexto do dispositivo determinado. A direção padrão do arco é no sentido anti-horário. Um aplicativo pode redefinir a direção do arco chamando a [**função SetArcDirection.**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection)

 

 
