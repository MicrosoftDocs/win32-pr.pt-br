---
title: Enumeração de formato de saída
description: Enumeração de formato de saída
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- SDK do Windows Media Format, enumerações de formato de saída
- ASF (Advanced Systems Format), enumerações de formato de saída
- ASF (formato de sistemas avançados), enumerações de formato de saída
- SDK do Windows Media Format, interface IWMReaderTypeNegotiation
- Formato de sistema avançado (ASF), interface IWMReaderTypeNegotiation
- ASF (formato de sistemas avançados), interface IWMReaderTypeNegotiation
- enumerações de formato de saída
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007066"
---
# <a name="output-format-enumeration"></a>Enumeração de formato de saída

O objeto leitor e o objeto leitor síncrono se comunicam com os codecs para enumerar os formatos de saída possíveis para fluxos compactados. Ao ler um arquivo com conteúdo compactado com um ou mais dos codecs de mídia do Windows, você pode examinar os possíveis formatos de saída para escolher aquele que melhor atenda às suas necessidades. Para sua conveniência, cada codec tem um formato de saída padrão que é definido para o formato usado com mais frequência. Para obter mais informações sobre a enumeração de saída, consulte [trabalhando com saídas](working-with-outputs.md).

Você pode fazer determinadas alterações em um formato de saída, dependendo do tipo de mídia. Para fluxos de vídeo, por exemplo, você pode alterar o tamanho do quadro e a intensidade da cor. Os objetos de leitura dão suporte a uma interface para testar as alterações feitas no formato de saída, chamado [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de leitura de arquivo**](file-reading-features.md)
</dt> </dl>

 

 




