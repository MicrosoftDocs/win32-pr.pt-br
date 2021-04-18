---
description: Usando o detector de mídia
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Usando o detector de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105778461"
---
# <a name="using-the-media-detector"></a>Usando o detector de mídia

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

O detector de mídia é um objeto auxiliar que pode recuperar informações sobre um arquivo, como o número de fluxos, seu tipo e sua duração. Ele também contém métodos para recuperar quadros de pôster de um fluxo de vídeo. Ele expõe a interface [**IMediaDet**](imediadet.md) .

O detector de mídia opera em um dos dois modos. Quando você cria uma instância do detector de mídia, ela não é anexada a um arquivo de origem específico. Nesse modo, você pode recuperar informações de fluxo de vários arquivos de origem. No entanto, depois de usar o detector de mídia para obter um quadro de pôster, ele alterna para o *modo de captura de bitmap*. No modo de captura de bitmap, o detector de mídia é anexado a um fluxo de vídeo específico e os métodos de informações de fluxo não funcionam mais. Além disso, não há como mudar o detector de mídia para seu modo de início. Portanto, obtenha as informações de fluxo necessárias antes de recuperar os quadros de pôster ou crie novas instâncias do detector de mídia para cada fluxo.

Para obter informações de fluxo, faça o seguinte:

1.  Chame [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) com o nome do arquivo de origem.
2.  Chame [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obter o número de fluxos na origem.
3.  Especifique um número de fluxo com [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md). Em seguida, chame um ou mais dos seguintes métodos:
    -   [**IMediaDet:: get \_ Streamtype**](imediadet-get-streamtype.md): recupera o tipo de mídia do fluxo.
    -   [**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md): recupera a duração do fluxo.
    -   [**IMediaDet:: get \_**](imediadet-get-framerate.md)Faixa de quadros: recupera a taxa de quadros de um fluxo de vídeo.

Para obter um quadro de cartaz, especifique o número do fluxo, como na etapa anterior. Em seguida, chame [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md), que copia um quadro de pôster em um buffer, ou [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md), que salva um quadro de pôster em um arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



