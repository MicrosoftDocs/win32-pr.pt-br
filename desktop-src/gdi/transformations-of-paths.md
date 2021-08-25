---
description: Os caminhos são definidos usando unidades lógicas e transformações atuais.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformações de caminhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7561cc1544a49555eaad4d58cf06d29a4763b6cd40528452c68cea551c99af34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888996"
---
# <a name="transformations-of-paths"></a>Transformações de caminhos

Os caminhos são definidos usando unidades lógicas e transformações atuais. (Se a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) tiver sido chamada, as unidades lógicas são unidades mundiais; caso contrário, as unidades lógicas são unidades de página.) Um aplicativo pode usar transformações mundiais para dimensionar, girar, distorcer, traduzir e refletir as linhas e as curvas Bézier que definem um caminho.

> [!Note]  
> Uma transformação do mundo dentro de um colchete só afeta as linhas e curvas desenhadas após a definição da transformação. Ele não terá nenhum efeito nessas linhas e curvas que foram desenhadas antes de ser definida. Para obter uma descrição da transformação do mundo, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).

 

Um aplicativo também pode usar [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para descrever a forma da caneta usada para descrever um caminho se a caneta for uma caneta geométrica. Para obter uma descrição das canetas geométricas, consulte [canetas](pens.md).

 

 



