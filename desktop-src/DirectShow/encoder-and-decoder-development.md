---
description: Codificador e desenvolvimento de decodificador
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Codificador e desenvolvimento de decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087617"
---
# <a name="encoder-and-decoder-development"></a>Codificador e desenvolvimento de decodificador

Esta seção contém artigos sobre o desenvolvimento de codificador e decodificador para o DirectShow. Esses tópicos não são relevantes para os desenvolvedores de aplicativos.

Um decodificador de software com suporte para o DirectX Video Acceleration (VA) deve ser implementado como um filtro de transformação de cópia do DirectShow. Se o decodificador não oferecer suporte ao DirectX VA, ele também poderá ser implementado como um DMO (objeto de mídia do DirectX). Um decodificador que se conecta a um processador de vídeo não deve ser implementado como um filtro de trans-in-Place, pois isso resultará em degradação de desempenho significativa. Para obter informações sobre como escrever um filtro de transformação de cópia, consulte [escrevendo filtros de transformação](writing-transform-filters.md).

Os codificadores de software podem ser implementados como filtros de transformação ou DMOs. Os codificadores não usam o DirectX VA, já que o DirectX VA atualmente é usado apenas para descompactação. A especificação da API do codificador descrita nesta seção é relevante para os codificadores de hardware e software.

Esta seção contém os seguintes tópicos:

-   [API do codificador](encoder-api.md)
-   [Interfaces e especificações do decodificador](decoder-interfaces-and-specifications.md)
-   [Configurações do decodificador para Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o VMR para desenvolvedores de filtro do DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



