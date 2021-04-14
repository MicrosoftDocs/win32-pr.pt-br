---
title: Trabalhando com entradas
description: Trabalhando com entradas
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- SDK do Windows Media Format, trabalhando com entradas
- ASF (Advanced Systems Format), trabalhando com entradas
- ASF (formato de sistemas avançados), trabalhando com entradas
- perfis, trabalhando com entradas
- fluxos, trabalhando com entradas
- codecs, trabalhando com entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453564"
---
# <a name="working-with-inputs"></a>Trabalhando com entradas

Assim como a configuração de fluxo adequada no perfil é necessária para obter o codec para compactar um fluxo, você também deve garantir que o tipo de mídia descompactada que você passa para o gravador seja descrito com precisão. Cada codec do Windows Media tem um tipo de entrada padrão associado, mas há suporte para vários tipos de entrada. Você pode examinar as entradas com suporte e selecionar aquela que corresponde aos seus dados. O processo de trabalho com entradas é resumido nas seguintes etapas:

1.  Quando você carrega um perfil para o gravador usar, o objeto do gravador atribui um número de entrada para cada conexão no perfil. Para obter mais informações sobre como carregar perfis para o gravador, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md). A menos que você esteja usando a exclusão mútua por taxa de bits, há uma conexão para cada fluxo. Os fluxos mutuamente exclusivos por taxa de bits compartilham uma única conexão.
2.  Seu aplicativo deve identificar os números de entrada para o arquivo. Para obter mais informações sobre como identificar números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).
3.  Para cada entrada, você deve garantir que o formato de entrada corresponda aos seus dados. Você pode enumerar os formatos de entrada com suporte no SDK. Para obter mais informações, consulte [para enumerar formatos de entrada](to-enumerate-input-formats.md). Você não pode enumerar os formatos de entrada de fluxos arbitrários ou fluxos que já estão compactados. Para obter mais informações sobre esses casos especiais, consulte [entradas de fluxo arbitrárias e precompactadas](arbitrary-and-precompressed-stream-inputs.md).
4.  Atribua o formato de entrada correto para cada conexão. Para obter mais informações, consulte [atribuindo formatos de entrada](assigning-input-formats.md).
5.  Alguns recursos de codec e gravador são configurados no momento da codificação em vez de no perfil. Para configurar esses recursos, você deve usar as configurações de entrada. Para obter mais informações, consulte [para definir as configurações de entrada](to-set-input-settings.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




