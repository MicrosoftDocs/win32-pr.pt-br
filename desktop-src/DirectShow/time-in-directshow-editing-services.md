---
description: Tempo nos serviços de edição do DirectShow
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Tempo nos serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421831742a2805f58d61c2258dad89d339131f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812810"
---
# <a name="time-in-directshow-editing-services"></a>Tempo nos serviços de edição do DirectShow

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Para editar o vídeo, você deve trabalhar com alguns conceitos de tempo importantes. Por exemplo:

-   Cada clipe tem uma duração.
-   Os clipes, as transições e os efeitos aparecem em determinados momentos em um projeto.
-   O vídeo tem uma taxa de quadros, expressa em quadros por segundo (FPS).

Os [serviços de edição do DirectShow](directshow-editing-services.md) (des) fornecem vários métodos que definem ou recuperam horas e taxas de quadros. O significado desses valores depende do contexto.

**Valores de tempo**

Quando um parâmetro expressa uma hora, três significados distintos são possíveis:

-   *Tempo da linha do* tempo: a hora relativa ao início da linha do tempo. Por exemplo, um clipe pode começar com 2 segundos na linha do tempo ou uma transição pode ocorrer 15 segundos na linha do tempo. A linha do tempo determina o projeto final renderizado, para que você também possa considerar a hora da linha do tempo como "hora do projeto".
-   *Hora da mídia*: um ponto em um arquivo de origem relativo ao início do arquivo, conforme atingido durante a reprodução normal. Por exemplo, se você tiver um arquivo de vídeo de 10 segundos, o ponto que percorrerá o arquivo ocorrerá em 5 minutos, expresso como um tempo de mídia.
-   *Hora do pai*: hora relativa a um objeto na linha do tempo. Por exemplo, se um objeto começa em 8 segundos na linha do tempo e contém outro objeto que começa em 10 segundos na linha do tempo, o objeto filho começa em 2 segundos em relação ao pai. Todas as faixas virtuais começam no tempo zero, em relação à linha do tempo. Portanto, para qualquer objeto em uma faixa virtual, a hora do pai é igual ao tempo da linha do tempo.

O tempo de mídia aplica-se somente a objetos de origem. Cada objeto de origem tem uma hora de início de mídia e uma hora de parada de mídia. Por exemplo, suponha que você tenha um clipe de vídeo de 10 segundos e deseje usar apenas 5 minutos do meio do clipe, cortando os primeiros 2 segundos e os últimos 3 segundos do clipe. Se você quiser que o clipe apareça 20 segundos no projeto (e supondo uma taxa de reprodução normal), você deverá especificar os seguintes horários de início e de parada.

-   Início da mídia: 2 segundos
-   Parada de mídia: 7 segundos
-   Início da linha do tempo: 20 segundos
-   Linha do tempo parada: 25 segundos

    ![inserindo um clipe de origem em uma linha do tempo](images/des-time1.png)

**Taxas de quadros**

A taxa de quadros é a "velocidade" de um fluxo de mídia, medida em quadros por segundo. Assim como ocorre com valores de hora, o significado de uma taxa de quadros depende do contexto:

-   **Taxa de quadros de saída:** A taxa de quadros do projeto renderizado final, definida pelo grupo. Quando você renderiza o projeto, cada grupo se torna um fluxo de mídia separado com sua própria taxa de quadros.
-   **Taxa de quadros de origem:** A taxa de quadros na qual o arquivo de origem foi originalmente criado. A taxa de quadros criados não precisa corresponder à taxa de quadros de saída do grupo. O DES fará automaticamente a amostragem ou a redução do arquivo conforme necessário. Para a maioria dos formatos de mídia, o DES pode determinar a taxa de quadros examinando o formato. Uma sequência DIB é uma exceção; Você deve especificar a taxa de quadros de uma sequência DIB. (Para obter mais informações, consulte [trabalhando com fontes](working-with-sources.md).)

**Taxa de reprodução:** A velocidade aparente de um clipe de origem quando ele aparece no projeto. Por exemplo, 10 segundos de vídeo pode ser ajustado em 5 segundos na linha do tempo. Como resultado, a velocidade do clipe aumenta em um fator de 2, como ilustra o diagrama a seguir.

![fazendo com que uma fonte seja executada mais rapidamente](images/des-time2.png)

(Com uma fonte de áudio, a densidade mudaria também.) A fórmula a seguir determina a taxa de reprodução do clipe de origem:

-   Taxa de reprodução = (parada de mídia – início da mídia)/(linha do tempo Stop – início da linha do tempo)

Observe que cada uma dessas três taxas é independente das outras:

-   Você pode acelerar ou reduzir um clipe ajustando os horários de mídia; Isso não afeta a taxa de quadros da saída final.
-   Você pode aumentar ou diminuir a taxa de quadros de saída sem afetar a velocidade de reprodução de um arquivo.
-   Você pode misturar, dentro do mesmo grupo, arquivos de origem que têm taxas de quadros criadas diferentes, e o DES fará amostras ou reduzirá a resolução de cada clipe para corresponder à taxa de quadros do grupo.

Quando você renderiza um projeto, todas as horas são arredondadas para o limite de quadro mais próximo, conforme determinado pela taxa de quadros do grupo. Por exemplo, suponha que um grupo de vídeos tenha uma taxa de quadros de 30 fps. Cada quadro tem aproximadamente 33 milissegundos (MS). Suponha que você adicione um clipe de origem de 1,68 segundos à linha do tempo, começando no tempo zero. A origem não termina exatamente em um limite de quadro, portanto, o DES arredonda o tempo de parada para 1,6666 segundos (50 quadros). Se você buscar 1,68 segundos no projeto renderizado, você realmente buscará após o final da origem, para o quadro 51 º.

No entanto, o DES não substitui a hora de parada da origem. Posteriormente, você pode alterar a taxa de quadros do grupo ou mover a origem para um novo ponto na linha do tempo em que ele arredonda de forma diferente. Portanto, o DES preserva a hora de parada original e arredonda somente quando necessário. Para obter mais informações, consulte [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com os serviços de edição do DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



