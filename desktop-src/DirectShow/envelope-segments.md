---
description: Segmentos de envelope
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmentos de envelope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500446"
---
# <a name="envelope-segments"></a>Segmentos de envelope

Uma curva de parâmetro consiste em um ou mais segmentos de envelope, definidos usando a estrutura de [**\_ \_ segmento de envelope MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) . Essa estrutura contém as seguintes informações:

-   Os horários de início e término.
-   Os valores inicial e final.
-   O tipo de curva (linear, quadrado e assim por diante).
-   Sinalizadores opcionais, descritos em breve.

O cliente adiciona segmentos de envelope a um parâmetro chamando o método [**IMediaParams:: addenvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) e passando uma matriz de estruturas **de \_ \_ segmento de envelope MP** . O cliente deve classificar os segmentos em ordem de tempo crescente antes de chamar o método. À medida que o DMO processa dados, você pode imaginar o parâmetro viajando em cada segmento de envelope, como um carro conduzindo uma série de Hills. O método [**IMediaParams:: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) retorna o valor mais recente.

Dois segmentos adjacentes podem ter uma lacuna entre eles. Durante as lacunas, o parâmetro retém seu valor anterior, da seguinte maneira:

-   Antes do primeiro segmento, o valor é o valor neutro.
-   Entre segmentos, o valor é o valor final do segmento anterior.
-   Após o último segmento, o valor permanece no valor final desse segmento.
-   Se o cliente liberar o DMO, o valor será revertido para o valor neutro.

Você pode alterar um segmento definindo qualquer um dos seguintes sinalizadores:

-   ENVLP do MPF \_ \_ begin \_ CURRENTVAL. O DMO usa o valor mais recente do parâmetro como o valor inicial para o segmento. Esse pode ser o valor neutro ou o valor final do segmento anterior. O DMO ignora o membro **valStart** da estrutura do **\_ \_ segmento de envelope do MP** .
-   ENVLP do MPF \_ \_ begin \_ NEUTRALVAL. O DMO usa o valor neutro do parâmetro como o valor inicial para o segmento. Ele ignora **valStart**.

Você pode considerar esses sinalizadores como captar o ponto inicial do segmento e movê-lo para cima ou para baixo, enquanto o valor final permanece fixo. O segmento será "alongar" de acordo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de mídia](media-parameters.md)
</dt> </dl>

 

 



