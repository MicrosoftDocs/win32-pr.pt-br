---
description: Tempo nos DirectShow de Edição
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Tempo nos DirectShow de Edição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc99ff2391ea7975daed7b4152e869741f9990561417131942c4d86e904fca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083608"
---
# <a name="time-in-directshow-editing-services"></a>Tempo nos DirectShow de Edição

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Para editar o vídeo, você deve trabalhar com alguns conceitos de tempo importantes. Por exemplo:

-   Cada clipe tem uma duração.
-   Clipes, transições e efeitos aparecem em determinados momentos em um projeto.
-   O vídeo tem uma taxa de quadros, expressa em quadros por segundo (fps).

[DirectShow DES (Serviços](directshow-editing-services.md) de Edição) fornece vários métodos que configuram ou recuperam tempos e taxas de quadros. O significado desses valores depende do contexto.

**Valores de tempo**

Quando um parâmetro expressa uma hora, três significados distintos são possíveis:

-   *Tempo da linha* do tempo: a hora relativa ao início da linha do tempo. Por exemplo, um clipe pode iniciar 2 segundos na linha do tempo ou uma transição pode ocorrer 15 segundos na linha do tempo. A linha do tempo determina o projeto renderizado final, para que você também possa pensar na hora da linha do tempo como "tempo do projeto".
-   *Tempo de mídia:* um ponto em um arquivo de origem relativo ao início do arquivo, conforme atingido durante a reprodução normal. Por exemplo, se você tiver um arquivo de vídeo de 10 segundos, o ponto no arquivo ocorrerá em 5 segundos, expresso como um tempo de mídia.
-   *Hora pai:* tempo relativo a um objeto na linha do tempo. Por exemplo, se um objeto for iniciado em 8 segundos na linha do tempo e contiver outro objeto que começa em 10 segundos na linha do tempo, o objeto filho será iniciado em 2 segundos em relação ao pai. As faixas virtuais começam na hora zero, em relação à linha do tempo. Portanto, para qualquer objeto em uma faixa virtual, a hora pai é igual à hora da linha do tempo.

O tempo de mídia aplica-se somente a objetos de origem. Cada objeto de origem tem uma hora de início de mídia e uma hora de parada de mídia. Por exemplo, suponha que você tenha um clipe de vídeo de 10 segundos e queira usar apenas 5 segundos do meio do clipe, recortando os primeiros 2 segundos e os últimos 3 segundos do clipe. Se você quiser que o clipe apareça 20 segundos no projeto (e supondo uma taxa de reprodução normal), especifique os horários de início e parada a seguir.

-   Início da mídia: 2 segundos
-   Parada de mídia: 7 segundos
-   Início da linha do tempo: 20 segundos
-   Parada da linha do tempo: 25 segundos

    ![inserindo um clipe de origem em uma linha do tempo](images/des-time1.png)

**Taxas de quadros**

Taxa de quadros é a "velocidade" de um fluxo de mídia, medida em quadros por segundo. Assim como com os valores de tempo, o significado de uma taxa de quadros depende do contexto:

-   **Taxa de quadros de saída:** A taxa de quadros do projeto renderizado final, definido pelo grupo. Quando você renderiza o projeto, cada grupo se torna um fluxo de mídia separado com sua própria taxa de quadros.
-   **Taxa de quadros de origem:** A taxa de quadros na qual o arquivo de origem foi originalmente autor. A taxa de quadros autorada não precisa corresponder à taxa de quadros de saída do grupo. O DES fará o upsample ou downsample automaticamente do arquivo conforme necessário. Para a maioria dos formatos de mídia, o DES pode determinar a taxa de quadros examinando o formato. Uma sequência DIB é uma exceção; você deve especificar a taxa de quadros de uma sequência DIB. (Para obter mais informações, consulte [Trabalhando com fontes](working-with-sources.md).)

**Taxa de reprodução:** A velocidade aparente de um clipe de origem quando ele aparece no projeto. Por exemplo, 10 segundos de vídeo podem ser encaixados em 5 segundos na linha do tempo. Como resultado, a velocidade do clipe aumenta em um fator de 2, como ilustra o diagrama a seguir.

![tornando uma reprodução de origem mais rápida](images/des-time2.png)

(Com uma fonte de áudio, a apresentação também seria deslocada.) A fórmula a seguir determina a taxa de reprodução de um clipe de origem:

-   Taxa de reprodução = (Parada de Mídia – Início da Mídia) / (Linha do Tempo – Início da Linha do Tempo)

Observe que cada uma dessas três taxas é independente das outras:

-   Você pode acelerar ou diminuir a velocidade de um clipe ajustando os tempos de mídia; isso não afeta a taxa de quadros da saída final.
-   Você pode aumentar ou diminuir a taxa de quadros de saída sem afetar a velocidade com que um arquivo é reproduzído.
-   Você pode combinar, dentro do mesmo grupo, arquivos de origem que têm taxas de quadros diferentes e o DES fará o aumento ou redução de cada clipe para corresponder à taxa de quadros do grupo.

Quando você renderiza um projeto, todas as vezes são arredondadas para o limite de quadro mais próximo, conforme determinado pela taxa de quadros do grupo. Por exemplo, suponha que um grupo de vídeos tenha uma taxa de quadros de 30 fps. Cada quadro tem aproximadamente 33 milissegundos (ms). Suponha que você adicione um clipe de origem de 1,68 segundo à linha do tempo, começando no tempo zero. A origem não termina exatamente em um limite de quadro, portanto, o DES faz a rodada do tempo de parada para 1,6666 segundos (50 quadros). Se você buscar 1,68 segundo no projeto renderizado, na verdade, buscará após o final da origem até o 51º quadro.

No entanto, o DES não substitui o tempo de parada da origem. Posteriormente, você pode alterar a taxa de quadros do grupo ou mover a origem para um novo ponto na linha do tempo em que ela é rodada de forma diferente. Portanto, o DES preserva a hora de parada original e é rodada somente quando necessário. Para obter mais informações, [**consulte IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com DirectShow de Edição](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



