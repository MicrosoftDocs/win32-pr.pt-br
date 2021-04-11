---
title: Para buscar pelo código de tempo SMPTE usando o leitor síncrono
description: Para buscar pelo código de tempo SMPTE usando o leitor síncrono
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Formato de sistemas avançados (ASF), buscando por códigos de tempo SMPTE
- ASF (formato de sistemas avançados), buscando por códigos de tempo SMPTE
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- leitores síncronos, buscando por códigos de tempo SMPTE
- leitores síncronos, códigos de tempo SMPTE
- Códigos de tempo SMPTE, buscando
- Códigos de tempo SMPTE, leitores síncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293790"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Para buscar pelo código de tempo SMPTE usando o leitor síncrono

O objeto leitor síncrono pode buscar um ponto em um arquivo com base no código de tempo SMPTE associado a um fluxo de vídeo. Os dados de código de tempo são encapsulados em estruturas de dados de extensão do código de WMT que são anexadas a amostras de vídeo como extensões de unidade de dados. [**\_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)

Os códigos de tempo SMPTE são definidos por um intervalo e um código de tempo dentro desse intervalo. Um intervalo é uma série contínua de códigos de tempo. Cada código de tempo é definido por horas, minutos, segundos e quadros.

Para buscar dados em um arquivo ASF pelo código de tempo SMPTE usando o leitor síncrono, execute as etapas a seguir.

1.  Defina o código de tempo de início e o código de tempo de término para a entrega de exemplo chamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Você deve especificar o número de fluxo de um fluxo de vídeo indexado por código de tempo. O leitor síncrono sincronizará o restante das saídas para a hora da apresentação do quadro especificado do fluxo especificado.
2.  Comece a recuperar exemplos com chamadas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Prossiga normalmente com o leitor síncrono.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Suporte ao código de tempo SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




