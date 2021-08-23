---
description: Definindo a taxa de reprodução
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Definindo a taxa de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0404e67d716616a4c383c134a4fb4e75060e3094023abec52df1d38099b92b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583316"
---
# <a name="setting-the-playback-rate"></a>Definindo a taxa de reprodução

Para alterar a taxa de reprodução, chame o [**método IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) Especifique a nova taxa como uma fração da taxa original. Por exemplo, para reproduzir em velocidade duas vezes normal, use o seguinte:


```C++
pSeek->SetRate(2.0)
```



Taxas maiores que uma são mais rápidas do que o normal. As taxas entre zero e uma são mais lentas do que o normal. Taxas negativas são definidas como reprodução regressiva, mas, na prática, a maioria dos filtros não é suportada. Atualmente, nenhum dos filtros padrão DirectShow suporte à reprodução inversa.

Independentemente da taxa de reprodução, a posição atual e a posição de parada são sempre expressas em relação à origem original. Por exemplo, se um arquivo de origem tiver 20 segundos de comprimento na taxa de reprodução normal, definir a posição atual como 10 segundos buscará o meio do arquivo. Se a taxa de reprodução for 2,0, a posição de parada for de 20 segundos e você buscar a posição de 10 segundos, o arquivo será reproduzir por 5 segundos de tempo real: 10 segundos, no dobro da velocidade de reprodução normal. A uma taxa de reprodução de 2,0, a posição atual aumenta duas vezes a taxa do relógio de referência.

 

 



