---
description: Uma pizza é uma região limitada pela interseção de uma curva de elipse e duas radials. A ilustração a seguir mostra uma pizza desenhada usando a função de pizza.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Sobre as tortas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010742"
---
# <a name="about-pies"></a>Sobre as tortas

Uma *pizza* é uma região limitada pela interseção de uma curva de elipse e duas radials. A ilustração a seguir mostra uma pizza desenhada usando a função de [**pizza**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .

![ilustração mostrando uma elipse com uma pizza sombreada](images/csfsh-03.png)

Ao chamar a [**pizza**](/windows/win32/api/wingdi/nf-wingdi-pie), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse, bem como as coordenadas de dois pontos que definem dois radials.

Quando o sistema desenha a parte curva da pizza, ele usa a direção do arco atual para o contexto do dispositivo fornecido. A direção do arco padrão é anti-horário. Um aplicativo pode redefinir a direção do arco chamando a função [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
