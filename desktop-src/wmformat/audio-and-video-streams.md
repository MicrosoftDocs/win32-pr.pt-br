---
title: Fluxos de áudio e vídeo
description: Fluxos de áudio e vídeo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- SDK do Windows Media Format, fluxos de áudio
- ASF (Advanced Systems Format), fluxos de áudio
- ASF (formato de sistemas avançados), fluxos de áudio
- SDK do Windows Media Format, fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos de áudio, sobre
- fluxos de vídeo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005449"
---
# <a name="audio-and-video-streams"></a>Fluxos de áudio e vídeo

Os tipos mais comuns de fluxos usados em arquivos criados com o Windows Media Format SDK são fluxos de áudio e vídeo. Representações digitais de dados de áudio e vídeo são complexas e ocupam grandes quantidades de memória. Na maioria das circunstâncias, áudio e vídeo são compactados antes de serem adicionados a um arquivo ASF. A compactação é realizada usando um compactador/descompactador (codec).

Vários codecs de mídia do Windows estão incluídos neste SDK e fornecem uma compactação de qualidade excelente para mídia digital. Para obter mais informações sobre os codecs de mídia do Windows, consulte [recursos de codec](codec-features.md). Muitos outros codecs estão disponíveis de várias fontes. Você pode usar quaisquer codecs que desejar ao criar arquivos ASF, mas somente os codecs do Windows Media são diretamente suportados pelos objetos deste SDK. Para usar outros codecs, você deve compactar amostras e passá-las para o objeto do gravador como dados arbitrários.

A distinção mais importante entre fluxos de áudio ou vídeo e fluxos arbitrários é que os fluxos que contêm dados de áudio ou vídeo do Windows Media são validados pelos objetos do SDK do Windows Media Format. Os fluxos de dados arbitrários não são validados automaticamente e devem ser verificados quanto à integridade pelo seu aplicativo.

As propriedades de um fluxo de áudio ou vídeo são descritas no perfil usado para criar o arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos arbitrários**](arbitrary-streams.md)
</dt> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




