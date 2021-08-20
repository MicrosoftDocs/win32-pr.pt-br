---
description: Descreve como armazenar dados Windows Mídia em um arquivo AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Armazenamento de mídia compactada em arquivos AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d52c33f6ea01cd1a10572294eaf3ee57ab4423567e3b2cc1f0feb86e199707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057721"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Armazenamento de mídia compactada em arquivos AVI (Microsoft Media Foundation)

Qualquer conteúdo compactado usando os codecs Windows Áudio de Mídia e Vídeo deve ser colocado em algum formato de contêiner. Um dos formatos mais populares é Intercalação de Vídeo de Áudio ou AVI. Você pode usar o Microsoft Video para Windows (VfW) ou o Microsoft DirectShow para criar arquivos AVI. Para obter mais informações sobre como usar o Video para Windows ou DirectShow, consulte a documentação do produto no MSDN.

Os codecs Windows Media Audio and Video foram desenvolvidos para usar as propriedades do ASF (Advanced Systems Format), que é o contêiner usado pelo Windows Media. Como o AVI e o ASF armazenam conteúdo de forma diferente, algumas dificuldades surgem ao armazenar conteúdo compactado com os codecs de áudio e vídeo de mídia Windows em um arquivo AVI.

Os Windows de áudio de mídia compactam o conteúdo de áudio de forma que ele não possa ser descompactado corretamente sem carimbos de data/hora para os exemplos individuais. Isso permite alguma otimização na mídia compactada. Como o contêiner asF mantém carimbos de data/hora com todos os exemplos, essa característica dos algoritmos de áudio sempre funcionou bem.

No entanto, os arquivos AVI não mantêm carimbos de data/hora com exemplos. Isso significa que Windows de áudio de mídia não pode ser descompactado corretamente quando armazenado em um arquivo AVI. Windows O conteúdo do Vídeo de Mídia não tem essa limitação e pode ser incluído em arquivos AVI. Para codificar Windows conteúdo de Vídeo de Mídia em um arquivo AVI com som sincronizado, você deve usar outro codec de áudio.

O outro problema com o uso de um arquivo AVI como um contêiner para Windows Mídia refere-se ao vídeo de baixa taxa de bits. Uma das maneiras pelas quais os codecs Windows Media Video produzem conteúdo de vídeo para taxas de bits baixas é soltando quadros duplicados. Se você quiser colocar o conteúdo do Windows Media Video em um arquivo ASF, será necessário definir o codificador para fornecer quadros fictícios para quadros duplicados (definir [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) como VARIANT TRUE) para que cada quadro seja representado \_ no arquivo. Os quadros fictícios produzidos pelo codec têm 8 bytes de tamanho. No entanto, o quadro gravado no arquivo pelo multiplexador AVI pode ser centenas de bytes maior e preenchido com dados aleatórios. Um arquivo AVI feito dessa maneira ainda será reproduzível, mas será muito maior do que o esperado. Você pode evitar esse problema usando taxas de bits mais altas ao codificar vídeo para armazenamento em arquivos AVI.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



