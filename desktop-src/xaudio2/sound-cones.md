---
description: Um modelo que descreve a intensidade de som orientado.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Cones de som
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814122"
---
# <a name="sound-cones"></a>Cones de som

Um modelo que descreve a intensidade de som orientado.

Um som sem orientação tem a mesma amplitude em uma determinada distância em todas as direções. Um som com uma orientação é mais alto na direção da orientação. O modelo que descreve a intensidade do som orientado é chamado de cone de som. Os cones de som são compostos de um cone interno (ou interno) e de um cone externo (ou externo). O ângulo de cone externo sempre deve ser igual ou maior que o ângulo de cone interno.

Em qualquer ângulo dentro do cone interno, o volume do som é definido como o volume de cone interno. Isso leva em conta o volume básico do buffer, a distância do ouvinte, a orientação do ouvinte, se o ouvinte tiver seu próprio cone e assim por diante.

Em qualquer ângulo fora do cone externo, o volume normal é atenuado por um fator definido pelo aplicativo. O nível de volume do cone externo é expresso como um dimensionador de amplitude linear: 1,0 f representa nenhuma atenuação aplicada ao sinal original, 0,5 f indica uma atenuação de 6 dB e 0,0 f resulta em silêncio. A amplificação (volume > 1,0 f) também é permitida e não é clamped. O intervalo de volume válido é de, na verdade, 0,0 f a 2,0 f.

Entre o cones interno e o externo está uma zona de transição do volume interno para o volume externo. O volume se aproxima do volume externo do cone conforme o ângulo aumenta.

Cones pode afetar parâmetros diferentes de volume. O nível de envio de filtro e reverberação de baixa aprovação também pode ser afetado, tornando a técnica ainda mais dramática. Por exemplo, com um cone no ouvinte, é possível especificar todos os sons por trás do ouvinte, obter um pouco de muffled e ter um conteúdo de taxa de reverberação um pouco maior. Eles fornecem mais indicações de que o som está atrás do usuário. Isso melhora o realm.

A ilustração a seguir mostra o conceito de cones de som.

![cones de som](images/common-audio-concepts-sound-cones.png)

A criação de som cones corretamente pode adicionar efeitos consideráveis ao seu aplicativo. Por exemplo, você pode posicionar uma fonte de som no centro de uma sala, definindo sua orientação em direção a uma porta aberta em um corredor. Em seguida, defina o ângulo do cone interior para que ele se estenda para a largura do porta, torne o cone horizontal um pouco mais largo e, por fim, defina o volume do cone externo como inaudível. Um ouvinte se mover ao longo do corredor começará a ouvir o som somente quando estiver próximo do porta. O som será mais alto quando o ouvinte passar na frente da porta aberta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos comuns de áudio](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**\_Cone X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



