---
title: Para recuperar exemplos compactados com o Leitor Síncrono
description: Para recuperar exemplos compactados com o Leitor Síncrono
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- ASF (Advanced Systems Format), recuperando amostras compactadas
- ASF (Formato de Sistemas Avançados), recuperando amostras compactadas
- ASF (Advanced Systems Format), leitores síncronos
- ASF (Formato de Sistemas Avançados), leitores síncronos
- ASF (Advanced Systems Format), amostras compactadas
- ASF (Formato de Sistemas Avançados), amostras compactadas
- leitores síncronos, recuperando amostras compactadas
- leitores síncronos, exemplos compactados
- amostras compactadas, recuperando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb2e3c7f1f6e00bd3f1c215a3b6783387fd3e19c268afe58862aa4b4d61889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807456"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Para recuperar exemplos compactados com o Leitor Síncrono

Assim como o leitor assíncrono, o leitor síncrono também pode recuperar amostras compactadas. Exemplos compactados devem ser usados ao copiar fluxos de um arquivo para outro.

O Windows SDK de Formato de Mídia não fornece nenhum método para decodificar dados depois que eles são extraídos de um arquivo ASF. Se você receber amostras compactadas e, posteriormente, quiser descompactá-las, será preciso fornecer seu próprio código para fazer isso. Uma maneira de obter essa limitação é gravar as amostras compactadas em um novo arquivo ASF e, em seguida, lê-las em exemplos normais e descompactados.

Para receber exemplos compactados com o leitor síncrono, chame [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) antes ou durante a reprodução. Passe true para *fCompressed.*

> [!Note]  
> Os fluxos de imagem não são válidos para entrega de fluxo compactado. Se você copiar um fluxo de imagem de um arquivo para outro, ele não funcionará no novo arquivo. Para copiar um fluxo de imagem de arquivo para arquivo, recupere os exemplos de fluxo de imagem por número de saída e inclua-os no novo arquivo como se estivesse incluindo um novo fluxo de imagem.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o Leitor Síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




