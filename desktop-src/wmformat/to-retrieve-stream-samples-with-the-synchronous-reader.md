---
title: Para recuperar exemplos de fluxo com o leitor síncrono
description: Para recuperar exemplos de fluxo com o leitor síncrono
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- ASF (Advanced Systems Format), recuperando amostras de fluxo
- ASF (formato de sistemas avançados), recuperando amostras de fluxo
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, recuperando amostras de fluxo
- fluxos, recuperando amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084350"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a>Para recuperar exemplos de fluxo com o leitor síncrono

Como o leitor assíncrono, o leitor síncrono pode recuperar amostras por número de fluxo. Ao contrário do leitor assíncrono, o leitor síncrono pode fornecer amostras de fluxo compactadas ou descompactadas.

Para receber amostras de fluxo, execute as etapas a seguir.

1.  A qualquer momento antes ou durante a reprodução, chame [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passando o número de fluxo desejado.
2.  Recupere exemplos com chamadas contínuas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).

Você pode verificar se um fluxo está selecionado para entrega de exemplo chamando [**IWMSyncReader:: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




