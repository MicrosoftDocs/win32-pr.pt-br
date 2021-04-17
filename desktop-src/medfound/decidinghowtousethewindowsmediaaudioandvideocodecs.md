---
description: Usando os objetos codec e DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Usando os objetos codec e DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761568"
---
# <a name="using-the-codec-and-dsp-objects"></a>Usando os objetos codec e DSP

Há várias maneiras de usar os codecs de áudio e vídeo do Windows Media e os DSPs para codificar, decodificar ou transformar seu conteúdo de mídia digital. O codec de áudio e vídeo do Windows Media e a API do DSP destinam-se a usuários que precisam configurar objetos codec e DSP manualmente ou usá-los fora do contexto de um dos SDKs do Windows Media, como o SDK do Windows Media Format ou SDK do Media Foundation.

Os criadores de conteúdo e os usuários finais podem usar uma variedade de ferramentas e aplicativos para codificar conteúdo em fluxos de vídeo de áudio do Windows ou Windows Media. O codificador de mídia do Windows, por exemplo, foi projetado especificamente para facilitar o processo de codificação. Da mesma forma, o Windows Media Player é especialmente projetado para funcionar bem com dados de mídia digital codificados nos formatos de mídia do Windows. Para muitos aplicativos, usar o SDK do Windows Media Encoder ou o SDK do Windows Media Player é tudo o que é necessário. Em particular, essas duas tecnologias são boas para cenários que se assemelham à funcionalidade das ferramentas que automatizam.

Se você precisar de mais controle sobre o processo de codificação ou decodificação, mas ainda pretende usar o ASF (Advanced Systems Format) como um contêiner para seus dados de mídia, o SDK do Windows Media Format pode ser uma boa opção. Os objetos do Windows Media Format SDK fornecem uma estrutura flexível para a criação de arquivos ASF e fornecem suporte interno para os codecs de vídeo e áudio do Windows Media.

O SDK do Media Foundation, que é novo para o Windows Vista, simplifica bastante a codificação e a decodificação fornecendo um pipeline de mídia personalizável. Você pode definir as propriedades de mídia de entrada e saída e o carregador de topologia de Media Foundation configurará os codecs e DSPs necessários para você.

O principal motivo para usar os objetos de codec diretamente é usar os codecs de áudio e vídeo do Windows Media fora do contêiner do ASF. O uso dos objetos codec e DSP também fornece um nível de controle que não está disponível usando qualquer uma das tecnologias mais abstratas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



