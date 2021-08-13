---
description: Descreve as estatísticas que você pode recuperar de um codec Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obter estatísticas de codificação (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa718a27894ea3e91faa953cb7b23e6c92b57c93d4b0fc0cf2c15b6995f28b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449156"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Obter estatísticas de codificação (Microsoft Media Foundation)

As informações sobre o que está acontecendo em uma sessão de codificação geralmente estão imediatamente disponíveis na forma de códigos de erro retornados ao processar exemplos. No entanto, há algumas estatísticas que você pode recuperar do codec sobre vários aspectos de codificação.

## <a name="video-frame-information"></a>Informações do quadro de vídeo

Algumas estatísticas de vídeo que você pode recuperar lidam com o número de quadros processados pelo codificador. Há três propriedades de número de quadro que você pode ler do codificador de vídeo:

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) é o número de quadros processados por meio do fluxo de entrada do DMO.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) é o número de quadros codificados. Ao subtrair esse valor do número total de quadros passados, você pode determinar quantos quadros foram descartados.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) é o número de quadros não codificados porque eles duplicaram o conteúdo já incluído. Esse valor não é subtraído do número de quadros codificados relatados pelo DMO.

Você pode ler as propriedades do quadro de vídeo a qualquer momento durante a codificação. Isso pode ser útil para determinar se as configurações de codificação são apropriadas para seu conteúdo; se houver uma grande diferença entre o total de quadros e quadros codificados, o conteúdo compactado poderá não atender aos seus requisitos de qualidade. Você pode ler os valores finais depois de concluir a codificação.

## <a name="vbr-buffer-statistics"></a>Estatísticas de buffer VBR

Dependendo do modo de codificação usado, algumas ou todas as configurações de buffer podem ser determinadas durante a codificação (por exemplo, a taxa de bits da VBR baseada em qualidade não é conhecida até que o conteúdo seja codificado). Há quatro propriedades de buffer VBR que você pode obter usando o **método IPropertyBag::Read:**

-   [MFPKEY \_ TAMBÉM É a](mfpkey-ravgproperty.md) taxa média de bits do conteúdo da VBR.
-   [MFPKEY \_ BAVG](mfpkey-bavgproperty.md) é a janela de buffer para a taxa média de bits.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) é a taxa de bits de pico do conteúdo da VBR.
-   [MFPKEY \_ BMAX é](mfpkey-bmaxproperty.md) a janela de buffer de pico.

Depois de começar a processar exemplos, você não deve ler nenhuma das propriedades do VBR até terminar de codificar o fluxo. Se você fizer isso, o codificador interpretará sua solicitação como um sinal de que a codificação está concluída. O próximo exemplo que você processa é tratado como uma nova sessão de codificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



