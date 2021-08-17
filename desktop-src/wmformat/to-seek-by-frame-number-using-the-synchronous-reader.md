---
title: Para buscar por número de quadro usando o leitor síncrono
description: Para buscar por número de quadro usando o leitor síncrono
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- ASF (Advanced Systems Format), buscando por números de quadro
- ASF (Formato de Sistemas Avançados), buscando por números de quadro
- ASF (Advanced Systems Format), leitores síncronos
- ASF (Formato de Sistemas Avançados), leitores síncronos
- leitores síncronos, buscando por números de quadro
- fluxos de vídeo, buscando por números de quadro
- fluxos de vídeo, leitores síncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b2da615f23e5c1d17046f08310d0aeda49200d5c4ba9fba890d7ba4951e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699107"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>Para buscar por número de quadro usando o leitor síncrono

Para buscar dados por número de quadro usando o leitor síncrono, especifique um intervalo para reprodução. Um intervalo é definido por um número de quadro inicial em um fluxo de vídeo específico e um número de quadros a reproduzir.

Para buscar dados em um arquivo ASF por número de quadro usando o leitor síncrono, execute as etapas a seguir.

1.  De definir o número do quadro inicial e o número de quadros a ler para entrega de exemplo chamando [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Você deve especificar o número de fluxo de um fluxo de vídeo indexado por quadro. O leitor sincroniza o restante das saídas com a hora de apresentação do quadro especificado do fluxo especificado e começa a fornecer exemplos de saída.
2.  Comece a recuperar exemplos com chamadas para [**IWMSyncReader::GetNextSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) Continue como faria normalmente com o leitor síncrono.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o Leitor Síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




