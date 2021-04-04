---
description: Descreve as estatísticas que você pode recuperar de um codec do Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtendo estatísticas de codificação (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646579"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Obtendo estatísticas de codificação (Microsoft Media Foundation)

As informações sobre o que está acontecendo em uma sessão de codificação geralmente estão imediatamente disponíveis na forma de códigos de erro retornados durante o processamento de amostras. No entanto, há algumas estatísticas que você pode recuperar do codec sobre vários aspectos de codificação.

## <a name="video-frame-information"></a>Informações de quadro de vídeo

Algumas estatísticas de vídeo que você pode recuperar tratam do número de quadros processados pelo codificador. Há três propriedades de número de quadro que você pode ler do codificador de vídeo:

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) é o número de quadros processados por meio do fluxo de entrada do DMO.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) é o número de quadros codificados. Ao subtrair esse valor do número total de quadros passados, você pode determinar quantos quadros foram descartados.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) é o número de quadros não codificados porque eles duplicaram o conteúdo já incluído. Esse valor não é subtraído do número de quadros codificados relatados pelo DMO.

Você pode ler as propriedades do quadro de vídeo a qualquer momento durante a codificação. Isso pode ser útil para determinar se as configurações de codificação são apropriadas para o seu conteúdo; Se houver uma grande diferença entre os quadros totais e os quadros codificados, o conteúdo compactado poderá não atender aos seus requisitos de qualidade. Você pode ler os valores finais depois de concluir a codificação.

## <a name="vbr-buffer-statistics"></a>Estatísticas de buffer de VBR

Dependendo do modo de codificação usado, algumas ou todas as configurações de buffer podem ser determinadas durante a codificação (por exemplo, a taxa de bits de VBR com base na qualidade não é conhecida até que o conteúdo seja codificado). Há quatro propriedades de buffer de VBR que você pode obter usando o método **IPropertyBag:: Read** :

-   [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) é a taxa de bits média do conteúdo da VBR.
-   [MFPKEY \_ BAVG](mfpkey-bavgproperty.md) é a janela de buffer para a taxa média de bits.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) é a taxa de bits de pico do conteúdo da VBR.
-   [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) é a janela de buffer de pico.

Depois de começar a processar os exemplos, você não deve ler nenhuma das propriedades de VBR até concluir a codificação do fluxo. Se você fizer isso, o codificador interpretará sua solicitação como um sinal de que a codificação foi concluída. O próximo exemplo que você processa é tratado como uma nova sessão de codificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



