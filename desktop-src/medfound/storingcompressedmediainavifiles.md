---
description: Descreve como armazenar dados de mídia do Windows em um arquivo AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Armazenando mídia compactada em arquivos AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297948"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Armazenando mídia compactada em arquivos AVI (Microsoft Media Foundation)

Qualquer conteúdo que você compactar usando os codecs de vídeo e áudio do Windows Media deve ser colocado em algum formato de contêiner. Um dos formatos mais populares é a intercalação de vídeo de áudio, ou AVI. Você pode usar o Microsoft Video para Windows (VfW) ou o Microsoft DirectShow para criar arquivos AVI. Para obter mais informações sobre como usar vídeo para Windows ou DirectShow, consulte a documentação do produto no MSDN.

Os codecs de áudio e vídeo do Windows Media foram desenvolvidos para usar as propriedades do ASF (Advanced Systems Format), que é o contêiner usado pelo Windows Media. Como o AVI e o ASF armazenam conteúdo de forma diferente, algumas dificuldades surgem ao armazenar o conteúdo compactado com os codecs de vídeo e áudio do Windows Media em um arquivo AVI.

Os codecs de áudio do Windows Media compactam o conteúdo de áudio de forma que ele não possa ser corretamente descompactado sem carimbos de data/hora para os exemplos individuais. Isso permite uma otimização na mídia compactada. Como o contêiner do ASF mantém carimbos de data/hora com todos os exemplos, essa característica dos algoritmos de áudio sempre funcionou bem.

Os arquivos AVI, no entanto, não mantêm carimbos de data/hora com exemplos. Isso significa que o conteúdo de áudio do Windows Media não pode ser descompactado corretamente quando armazenado em um arquivo AVI. O conteúdo de vídeo do Windows Media não tem essa limitação e pode ser incluído em arquivos AVI. Para codificar o conteúdo de vídeo do Windows Media em um arquivo AVI com som sincronizado, você deve usar outro codec de áudio.

O outro problema com o uso de um arquivo AVI como um contêiner para o Windows Media está relacionado ao vídeo de baixa taxa de bits. Uma das maneiras pelas quais os codecs de vídeo do Windows Media produzem conteúdo de vídeo para taxas de bits baixas é descartando os quadros duplicados. Se você quiser colocar o conteúdo de vídeo do Windows Media em um arquivo ASF, precisará definir o codificador para entregar quadros fictícios para quadros duplicados (Set [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to Variant \_ true) para que cada quadro seja representado no arquivo. Os quadros fictícios produzidos pelo codec têm 8 bytes de tamanho. No entanto, o quadro gravado no arquivo pelo multiplexador AVI pode ser de centenas de bytes maiores e preenchido com dados aleatórios. Um arquivo AVI feito dessa maneira ainda será reproduzido, mas será muito maior do que o esperado. Você pode evitar esse problema usando taxas de bits mais altas ao codificar vídeo para armazenamento em arquivos AVI.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



