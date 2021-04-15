---
description: Este tópico descreve como a origem do sequenciador lida com os tempos de apresentação durante a reprodução.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Tempos de apresentação da sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17f5b0ff4bd6f0cfee2b1b461d6fbd11bdbf0fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502250"
---
# <a name="sequence-presentation-times"></a>Tempos de apresentação da sequência

Este tópico descreve como a [origem do sequenciador](sequencer-source.md) lida com os tempos de apresentação durante a reprodução.

## <a name="overview"></a>Visão geral

A origem do sequenciador dá suporte a dois modos diferentes: sequências de playlist e sequências de edição.

Em uma sequência de edição, o aplicativo especifica a duração de cada segmento com antecedência, antes de iniciar a reprodução. Em uma sequência de playlist, o aplicativo não especifica a duração antecipadamente. (Na verdade, a duração pode não ser conhecida.)

Em ambos os casos, você pode especificar a hora de início e de parada de mídia de um segmento. Essas vezes especificam a posição no arquivo de origem onde o segmento começa e termina. Por exemplo, suponha que o arquivo de origem tenha 90 segundos de comprimento. Se você quisesse cortar os primeiros 10 segundos e os últimos 10 segundos, você especificaria os seguintes valores:

-   Início da mídia: 10 segundos
-   Parada de mídia: 80 segundos

Para especificar a hora de início da mídia, defina o atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) no nó de origem. Para especificar a hora de parada da mídia, defina o atributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) no nó de origem.

Para criar uma sequência de edição, defina o atributo [ \_ \_ \_ tempo global de sessão MF](mf-session-global-time-attribute.md) ao criar a sessão de mídia. Caso contrário, a sessão de mídia espera sequências de playlist. Em uma sequência de edição, cada topologia de segmento deve ter o atributo [ \_ \_ PROJECTSTART de topologia MF](mf-topology-projectstart-attribute.md) e o atributo [ \_ \_ PROJECTSTOP de topologia MF](mf-topology-projectstop-attribute.md) .

## <a name="playlist-sequences"></a>Sequências de playlist

Em uma sequência de playlist, o relógio de apresentação começa em zero e continua em limites de segmento. As fontes nativas entregam amostras com carimbos de data/hora iguais ao tempo de mídia. O pipeline converte os carimbos de data/hora para o horário de apresentação correto da seguinte maneira:

-   Novo carimbo de data/hora = tempo de mídia + deslocamento − início da mídia

O valor de *offset* é a hora da apresentação na qual o segmento anterior terminou. Para o primeiro segmento, o deslocamento é zero. Aqui estão dois exemplos de como essas conversões de carimbo de data/hora são calculadas:

-   Exemplo 1: Suponha que o primeiro segmento (S1) tenha 10 segundos de comprimento e o segundo segmento (S2) tenha uma hora de início de mídia igual a zero. A origem nativa usa o tempo de mídia para seus carimbos de data/hora, portanto, a primeira amostra de S2 tem um carimbo de data/hora igual a zero. O deslocamento é de 10 segundos (a duração de S1), portanto, o carimbo de data/hora ajustado é: 0 + 10 − 0 = 10 segundos.
-   Exemplo 2: Suponha que o segmento S1 seja de 10 segundos e S2 tenha uma hora de início da mídia de 5 segundos. A primeira amostra de S2 tem um carimbo de data/hora de 5 segundos (tempo de mídia). O deslocamento é de 10 segundos, portanto, o carimbo de data/hora ajustado é: 5 + 10 − 5 = 10 segundos.

Todos os componentes de pipeline downstream dos nós de origem recebem exemplos com os carimbos de data/hora ajustados. Os nós de origem em uma topologia podem ter horários de início de mídia diferentes, portanto, os ajustes são calculados separadamente para cada ramificação da topologia.

Quando a apresentação muda para o próximo segmento, o relógio de apresentação não é interrompido ou redefinido, e o tempo de apresentação aumenta de forma monotônico. Antes do início de um novo segmento, a sessão de mídia envia ao aplicativo um evento [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) . O evento especifica a hora de início do segmento, em relação ao relógio de apresentação e o valor do deslocamento. Quando um novo segmento é iniciado, o pipeline chama o [**início**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) na origem do sequenciador com o valor VT \_ vazio. A origem do sequenciador envia um evento [MESourceStarted](mesourcestarted.md) sem hora de início.

Para buscar, o aplicativo especifica um identificador de segmento mais um deslocamento de tempo dentro do segmento. Após a busca, o relógio de apresentação começa no deslocamento do *segmento* . Veja um exemplo de como esse processo funciona:

-   Exemplo 3: o aplicativo busca segmentar S3, com um deslocamento de segmento de 10 segundos. O relógio de apresentação começa em 10 segundos (o deslocamento de segmento). O deslocamento não inclui a duração dos segmentos S1 e S2. A origem do sequenciador envia um evento [MESourceStarted](mesourcestarted.md) com uma hora de início igual ao deslocamento do segmento, 10 segundos.

Após uma busca, se a reprodução continuar para o próximo segmento, a transição funcionará da mesma forma que os exemplos anteriores, exceto pelo fato de que o deslocamento não inclui os segmentos ignorados.

Aqui estão alguns detalhes adicionais que afetam como os exemplos são carimbados por tempo:

-   Os decodificadores podem precisar de dados além da hora de parada da mídia. O pipeline recebe o máximo de dados da origem que o decodificador requer e, em seguida, corta os exemplos de saída do decodificador.
-   As transformações podem armazenar dados em buffer. Por exemplo, um efeito de áudio pode precisar fazer isso. Quando um segmento termina, o carimbo de data/hora na última amostra da transformação é anterior ao final do segmento, porque a transformação está revertendo alguns dados. Quando o próximo segmento é iniciado, o carimbo de data/hora no primeiro exemplo é ligeiramente anterior ao início do segmento. Não há nenhum intervalo nos carimbos de data/hora, portanto, os dados que atingem o coletor de mídia são contínuos. Quando o segmento final termina, o pipeline esvazia a transformação, portanto, nenhum dado é perdido.
-   A fonte pode precisar iniciar um pouco antes da hora de início da mídia para selecionar o quadro-chave anterior. Portanto, após o ajuste, o primeiro exemplo pode ter um tempo de apresentação negativo.

## <a name="editing-sequences"></a>Sequências de edição

Em uma sequência de edição, o aplicativo especifica os limites de segmento antecipadamente, definindo os atributos de topologia [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) e [**MF Topology \_ \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) . O pipeline calcula os ajustes para os carimbos de data/hora quase da mesma maneira que para uma sequência de playlist:

-   Para o deslocamento, ele usa o valor de [**\_ \_ PROJECTSTART de topologia MF**](mf-topology-projectstart-attribute.md), em vez de usar a extremidade observada do segmento.

-   Para procurar, o deslocamento usa um valor igual ao valor de [**PROJECTSTART da \_ topologia \_ MF**](mf-topology-projectstart-attribute.md) do segmento mais o deslocamento do segmento.

Portanto, o tempo de apresentação em uma sequência de edição é sempre relativo ao início da apresentação, mesmo se o aplicativo busca outro segmento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 



