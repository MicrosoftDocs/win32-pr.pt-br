---
description: Os registros de spline representam as curvas quadráticas (isto é, linha de b quadrática) usadas por TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Registros de spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661966"
---
# <a name="spline-records"></a>Registros de spline

Os registros de spline representam as curvas quadráticas (isto é, linha de b quadrática) usadas por TrueType. Um registro de spline começa com o último ponto no registro anterior (ou para o primeiro registro na delimitação, com o ponto de partida). Para o primeiro registro spline, o ponto inicial e o último ponto no registro estão no contorno de glifo. Para todos os outros registros de spline, apenas o último ponto está no contorno de glifo. Todos os outros pontos nos registros de spline estão fora do contorno de glifo e devem ser renderizados como os pontos de controle de linhas b.

O último registro de spline ou polilinha em uma delimitação sempre termina com o ponto inicial da delimitação. Essa organização garante que cada contorno seja fechado.

Como as splines b exigem três pontos (um ponto fora do contorno de glifo entre dois pontos que estão na estrutura de tópicos), você deve executar alguns cálculos quando um registro spline contiver mais de um ponto fora da curva.

Por exemplo, se um registro de spline contiver três pontos (A, B e C) e não for o primeiro registro, os pontos A e B estarão fora do contorno de glifo. Para interpretar o ponto A, use a posição atual (que sempre está no contorno do glifo) e o ponto na estrutura de tópicos do glifo entre os pontos A e B. Para localizar o ponto médio (M) entre A e B, você pode executar o cálculo a seguir.

M = A + (B A)/2

O ponto médio entre os pontos fora da estrutura de tópicos consecutivos em um registro spline é um ponto no contorno do glifo, de acordo com a definição do formato spline usado em fontes TrueType.

Se a posição atual for designada por P, as duas splines quadráticas definidas por esse registro spline serão (P, A, M) e (M, B, C).

 

 



