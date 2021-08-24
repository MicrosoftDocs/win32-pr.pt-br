---
description: Os registros spline representam as curvas quadráticas (ou seja, b-splines quadráticas) usadas por TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Spline Records
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbaf3730f327501bd55b2e35b9410f03fd0559cbb5e36d87a3052901d26e5f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613646"
---
# <a name="spline-records"></a>Spline Records

Os registros spline representam as curvas quadráticas (ou seja, b-splines quadráticas) usadas por TrueType. Um registro spline começa com o último ponto no registro anterior (ou para o primeiro registro no mapa, com o ponto de partida). Para o primeiro registro spline, o ponto inicial e o último ponto no registro estão no contorno de glifo. Para todos os outros registros spline, somente o último ponto está no contorno de glifo. Todos os outros pontos nos registros spline estão fora do contorno de glifo e devem ser renderizados como os pontos de controle de b-splines.

O último registro de spline ou polilinha em um contorno sempre termina com o ponto de partida do sr. Essa disposição garante que todos os contornos são fechados.

Como b-splines exigem três pontos (um ponto fora do contorno de glifo entre dois pontos que estão no contorno), você deve executar alguns cálculos quando um registro spline contiver mais de um ponto fora da curva.

Por exemplo, se um registro spline contiver três pontos (A, B e C) e não for o primeiro registro, os pontos A e B serão fora do contorno do glifo. Para interpretar o ponto A, use a posição atual (que está sempre no contorno do glifo) e o ponto no contorno de glifo entre os pontos A e B. Para encontrar o ponto médio (M) entre A e B, você pode executar o cálculo a seguir.

M = A + (B A)/2

O ponto médio entre pontos fora do contorno consecutivos em um registro spline é um ponto no contorno de glifo, de acordo com a definição do formato spline usado em fontes TrueType.

Se a posição atual for designada por P, os dois splines quadráticos definidos por esse registro spline serão (P, A, M) e (M, B, C).

 

 



