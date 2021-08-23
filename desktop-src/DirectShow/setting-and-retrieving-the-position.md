---
description: Configurando e recuperando a posição
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Configurando e recuperando a posição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7951ce12fe498a4f230ab3d1ac84796621e04ed025010678f1c43a39d88eb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683686"
---
# <a name="setting-and-retrieving-the-position"></a>Configurando e recuperando a posição

O grafo de filtro mantém dois valores de posição, posição atual e posição de parada. Eles são definidos da seguinte maneira:

-   Quando o grafo está em execução, a posição atual é a posição de reprodução atual, relativa ao início da origem. Quando o grafo é interrompido ou pausado, a posição atual é o ponto em que o streaming começará no próximo comando de execução.
-   A posição de parada é o ponto em que o fluxo será encerrado. Quando o grafo atinge a posição de parada, nenhum dado é transmitido e o Gerenciador de gráfico de filtro posta um evento de [**\_ conclusão de EC**](ec-complete.md) . (No entanto, o grafo não muda automaticamente para um estado parado. Para obter mais informações, consulte [respondendo a eventos](responding-to-events.md).)

Para recuperar esses valores, chame o método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) . Os valores retornados são sempre relativos à origem da mídia original. Por padrão, os valores estão em unidades de tempo de referência. Em alguns casos, você pode alterar as unidades de tempo; para obter mais informações, consulte [formatos de hora para comandos de busca](time-formats-for-seek-commands.md).

Para buscar uma nova posição ou definir uma nova posição de parada, chame o método [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , conforme mostrado no exemplo a seguir:


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> Um segundo é de 10 milhões unidades de tempo de referência. Para sua conveniência, o exemplo define esse valor como um \_ segundo. se você estiver usando a biblioteca de classe base DirectShow, as unidades de constante têm o mesmo valor.

 

O parâmetro *rtNow* especifica a nova posição atual. O segundo parâmetro é um sinalizador que define como interpretar *rtNow*. Neste exemplo, o sinalizador AM \_ buscando \_ AbsolutePositioning indica que *rtNow* especifica uma posição absoluta na origem. Portanto, o grafo de filtro vai procurar uma posição de dois segundos desde o início do fluxo. O parâmetro *rtStop* fornece a hora de parada. O último parâmetro especifica que *rtStop* também é uma posição absoluta.

Para especificar uma posição relativa ao valor da posição anterior, use o \_ sinalizador am buscando \_ RelativePositioning. Para deixar um dos valores de posição inalterados, use o \_ sinalizador am buscando sem \_ posicionamento. O parâmetro time correspondente pode ser **nulo** nesse caso. O exemplo a seguir busca avançar por 10 segundos, mas deixa a posição de parada inalterada:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Se o grafo de filtro for interrompido, o processador de vídeo não atualizará a imagem após uma operação de busca. Para o usuário, ele aparecerá como se a busca não tivesse acontecido. Para atualizar a imagem, pause o grafo após a operação de busca. Pausar o grafo aponta um novo quadro de vídeo para o processador de vídeo. Você pode usar o método [**IMediaControl:: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , que pausa o grafo e o interrompe.

 

 



