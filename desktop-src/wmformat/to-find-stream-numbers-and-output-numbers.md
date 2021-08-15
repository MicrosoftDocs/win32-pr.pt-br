---
title: Para encontrar números de fluxo e números de saída
description: Para encontrar números de fluxo e números de saída
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- FORMATO DE SISTEMAS Avançados (ASF), números de fluxo
- ASF (Formato de Sistemas Avançados), criando números
- ASF (Advanced Systems Format), localizar números de saída
- ASF (Formato de Sistemas Avançados), localizar números de saída
- leitores síncronos, números de fluxo
- leitores síncronos, encontrando números de saída
- fluxos, localizar números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699584"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Para encontrar números de fluxo e números de saída

O leitor síncrono dá suporte à alternação mais simplificada entre números de fluxo e saída para reprodução do que o leitor assíncrono. Portanto, é mais importante ser capaz de encontrar quais números de fluxo equivalem a quais números de saída ou o contrário.

Para encontrar o número de saída que corresponde a um número de fluxo, chame [**IWMSyncReader::GetOutputNumberForStream.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream)

Para encontrar o número de fluxo que corresponde a um número de saída, chame [ **IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lendo arquivos com o Leitor Síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




