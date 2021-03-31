---
title: Para localizar números de fluxo e números de saída
description: Para localizar números de fluxo e números de saída
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- ASF (Advanced Systems Format), números de fluxo
- ASF (formato de sistemas avançados), criando números
- ASF (Advanced Systems Format), localizando números de saída
- ASF (formato de sistemas avançados), localizando números de saída
- leitores síncronos, números de fluxo
- leitores síncronos, localizando números de saída
- fluxos, localizando números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640137"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Para localizar números de fluxo e números de saída

O leitor síncrono dá suporte à alternância mais simplificada entre os números de fluxo e de saída para reprodução do que o leitor assíncrono. Portanto, é mais importante encontrar quais números de fluxo são equivalentes aos números de saída ou ao contrário.

Para localizar o número de saída que corresponde a um número de fluxo, chame [**IWMSyncReader:: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Para localizar o número de fluxo que corresponde a um número de saída, chame [ **IWMSyncReader:: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Entradas, fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




