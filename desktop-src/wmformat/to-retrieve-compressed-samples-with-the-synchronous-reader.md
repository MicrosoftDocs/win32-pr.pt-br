---
title: Para recuperar amostras compactadas com o leitor síncrono
description: Para recuperar amostras compactadas com o leitor síncrono
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- ASF (Advanced Systems Format), recuperando amostras compactadas
- ASF (formato de sistemas avançados), recuperando amostras compactadas
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- ASF (Advanced Systems Format), amostras compactadas
- ASF (formato de sistemas avançados), amostras compactadas
- leitores síncronos, recuperando amostras compactadas
- leitores síncronos, amostras compactadas
- amostras compactadas, recuperando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084352"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Para recuperar amostras compactadas com o leitor síncrono

Como o leitor assíncrono, o leitor síncrono também pode recuperar amostras compactadas. Amostras compactadas devem ser usadas ao copiar fluxos de um arquivo para outro.

O Windows Media Format SDK não fornece nenhum método para decodificar dados depois que ele foi extraído de um arquivo ASF. Se você receber amostras compactadas e, posteriormente, quiser descompactá-las, precisará fornecer seu próprio código para fazer isso. Uma maneira de contornar essa limitação é escrever os exemplos compactados em um novo arquivo ASF e, em seguida, lê-los novamente em amostras normais e descompactadas.

Para receber amostras compactadas com o leitor síncrono, chame [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) antes ou durante a reprodução. Passe true para *fCompressed*.

> [!Note]  
> Fluxos de imagem não são válidos para entrega de fluxo compactado. Se você copiar um fluxo de imagem de um arquivo para outro, ele não funcionará no novo arquivo. Para copiar um fluxo de imagem do arquivo para o arquivo, recupere os exemplos de fluxo de imagem por número de saída e inclua-os no novo arquivo como se incluir um novo fluxo de imagem.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




