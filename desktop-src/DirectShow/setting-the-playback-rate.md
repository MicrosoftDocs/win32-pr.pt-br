---
description: Definindo a taxa de reprodução
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Definindo a taxa de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105767668"
---
# <a name="setting-the-playback-rate"></a>Definindo a taxa de reprodução

Para alterar a taxa de reprodução, chame o método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) . Especifique a nova taxa como uma fração da taxa original. Por exemplo, para reproduzir em velocidade de duas vezes-normal, use o seguinte:


```C++
pSeek->SetRate(2.0)
```



As taxas maiores que um são mais rápidas do que o normal. As taxas entre zero e uma são mais lentas do que o normal. As taxas negativas são definidas como reprodução regressiva, mas na prática a maioria dos filtros não oferece suporte a ela. Atualmente, nenhum dos filtros do DirectShow padrão oferece suporte à reprodução inversa.

Independentemente da taxa de reprodução, a posição atual e a posição de parada são sempre expressas em relação à fonte original. Por exemplo, se um arquivo de origem tiver 20 segundos de duração na taxa de reprodução normal, definir a posição atual como 10 segundos irá procurar o meio do arquivo. Se a taxa de reprodução for 2,0, a posição de parada será de 20 segundos e você procurar a posição de 10 segundos, o arquivo será executado por 5 minutos de tempo real: 10 segundos de importância, com duas vezes a velocidade de reprodução normal. Em uma taxa de reprodução de 2,0, a posição atual aumenta em duas vezes a taxa do relógio de referência.

 

 



