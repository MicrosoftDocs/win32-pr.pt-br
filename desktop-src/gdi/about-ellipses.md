---
description: Uma elipse é uma curva fechada definida por dois pontos fixos (F1 e F2), de modo que a soma das distâncias (D1 + D2) de qualquer ponto na curva até os dois pontos fixos seja constante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Sobre reticências
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550945"
---
# <a name="about-ellipses"></a>Sobre reticências

Uma elipse é uma curva fechada definida por dois pontos fixos (F1 e F2), de modo que a soma das distâncias (D1 + D2) de qualquer ponto na curva até os dois pontos fixos seja constante. A ilustração a seguir mostra uma elipse desenhada usando a função [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .

![ilustração mostrando uma elipse, dois pontos fixos, duas distâncias e um retângulo delimitador](images/csfsh-01.png)

Ao chamar [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse. Um *retângulo delimitador* é o menor retângulo ao redor da elipse. Quando o sistema desenha a elipse, ele exclui os lados direito e inferior se nenhuma transformação mundial for definida. Portanto, para qualquer retângulo medindo x unidades de largura por unidades y alta, a elipse associada mede as unidades X1 de largura por Y1 unidades de altura. Se o aplicativo definir uma transformação do mundo chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , o sistema incluirá os lados direito e inferior.

 

 



