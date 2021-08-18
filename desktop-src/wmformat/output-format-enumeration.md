---
title: Enumeração de formato de saída
description: Enumeração de formato de saída
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows SDK de Formato de Mídia, enumerações de formato de saída
- ASF (Advanced Systems Format), enumerações de formato de saída
- ASF (Formato de Sistemas Avançados), enumerações de formato de saída
- Windows SDK de Formato de Mídia, interface IWMReaderTypeNegotiation
- AsF (Advanced Systems Format), interface IWMReaderTypeNegotiation
- ASF (formato de sistemas avançados), interface IWMReaderTypeNegotiation
- enumerações de formato de saída
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd1e6dacf4daac3f8c5f74fa1b4d9dd83c5cb3be538dc983b671a9f9096325f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027354"
---
# <a name="output-format-enumeration"></a>Enumeração de formato de saída

O objeto leitor e o objeto de leitor síncrono se comunicam com os codecs para enumerar os possíveis formatos de saída para fluxos compactados. Ao ler um arquivo que contém conteúdo compactado com um ou mais dos codecs Windows Media, você pode examinar os possíveis formatos de saída para escolher aquele que melhor atende às suas necessidades. Para sua conveniência, cada codec tem um formato de saída padrão que é definido para o formato mais usado. Para obter mais informações sobre a enumeração de saída, consulte [Trabalhando com saídas](working-with-outputs.md).

Você pode fazer determinadas alterações em um formato de saída dependendo do tipo de mídia. Para fluxos de vídeo, por exemplo, você pode alterar o tamanho do quadro e a profundidade da cor. Os objetos de leitura suportam uma interface para testar as alterações feitas no formato de saída, chamada [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de leitura de arquivo**](file-reading-features.md)
</dt> </dl>

 

 




