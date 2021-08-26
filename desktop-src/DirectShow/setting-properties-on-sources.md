---
description: Definindo propriedades em fontes
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Definindo propriedades em fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06908f4f15a6d1107ce15e71679c92ec8065725ed883a6561df5cd21af3e13c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965016"
---
# <a name="setting-properties-on-sources"></a>Definindo propriedades em fontes

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Quando você cria um novo objeto de origem, há algumas propriedades que você precisa definir e outras que você pode definir como opção. Você deve definir as propriedades a seguir.

-   Os horários de início e de término, em relação ao restante da linha do tempo. Chame o método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) . Não defina os horários sobrepostos em objetos de origem dentro da mesma faixa ou causará um comportamento indefinido.
-   O arquivo de mídia a ser usado como um clipe de origem. Chame o [**IAMTimelineSrc:: Setmedianame**](iamtimelinesrc-setmedianame.md).
-   As horas de início e de parada da mídia em relação ao arquivo de origem original. Chame o método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Exceção: se a origem for uma imagem ainda, não especifique os horários de mídia. para obter mais informações sobre os tempos de mídia, consulte [tempo em DirectShow serviços de edição](time-in-directshow-editing-services.md).

Um objeto de origem herda seu tipo de mídia do grupo pai, portanto, não é necessário especificar um tipo de mídia.

As propriedades opcionais incluem o seguinte:

-   O modo de ampliação. o modo de ampliação especifica como o Microsoft® DirectShow serviços de edição de® (DES) renderiza uma fonte cujo tamanho não corresponde às dimensões de saída. Por padrão, o DES alonga uma imagem sem preservar a taxa de proporção. Como alternativa, o DES pode cortar uma imagem ou criar um letterbox. Chame o método [**IAMTimelineSrc:: Setstretchmode**](iamtimelinesrc-setstretchmode.md) para especificar o modo de ampliação.
-   A duração do arquivo de origem. Se você definir essa propriedade antes de definir os horários de mídia, o DES validará a hora de parada da mídia e truncará a hora de parada se ela exceder a duração do arquivo. Isso pode ajudar a evitar erros de renderização posteriormente. Você pode obter a duração do arquivo usando o detector de mídia, conforme descrito em [usando o detector de mídia](using-the-media-detector.md). Chame o método [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md) para especificar a duração do arquivo.
-   O número do fluxo. Por padrão, um objeto de origem usa o primeiro fluxo no arquivo que corresponde ao tipo de mídia do grupo pai. Se um arquivo contiver dois ou mais fluxos do mesmo tipo de mídia, selecione qual fluxo usar chamando [**IAMTimelineSrc:: SetStreamNumber**](iamtimelinesrc-setstreamnumber.md). Você pode usar o detector de mídia para localizar o número de fluxos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



