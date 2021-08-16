---
title: Para buscar pelo código de tempo SMPTE usando o leitor síncrono
description: Para buscar pelo código de tempo SMPTE usando o leitor síncrono
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- ASF (Advanced Systems Format), buscando por códigos de tempo SMPTE
- ASF (Formato de Sistemas Avançados), buscando por códigos de tempo SMPTE
- ASF (Advanced Systems Format), leitores síncronos
- ASF (Formato de Sistemas Avançados), leitores síncronos
- AsF (Advanced Systems Format), códigos de hora SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- leitores síncronos, buscando por códigos de tempo SMPTE
- leitores síncronos, códigos de tempo SMPTE
- Códigos de tempo SMPTE, buscando
- Códigos de tempo SMPTE, leitores síncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b368492d45d3bc564ce0fbb84a6013349c26fcdaca8c1ad576863a9cee6f6f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196465"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Para buscar pelo código de tempo SMPTE usando o leitor síncrono

O objeto de leitor síncrono pode buscar até um ponto em um arquivo com base no código de tempo SMPTE associado a um fluxo de vídeo. Os dados de código de hora são encapsulados em estruturas de DADOS DE EXTENSÃO [**DO WMT \_ TIMECODE \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) anexadas a exemplos de vídeo como extensões de unidade de dados.

Os códigos de tempo SMPTE são definidos por um intervalo e um código de tempo dentro desse intervalo. Um intervalo é uma série contínua de códigos de tempo. Cada código de hora é definido por horas, minutos, segundos e quadros.

Para buscar dados em um arquivo ASF por código de hora SMPTE usando o leitor síncrono, execute as etapas a seguir.

1.  De definir o código de hora inicial e o código de hora final para entrega de exemplo chamando [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Você deve especificar o número de fluxo de um fluxo de vídeo indexado por código de tempo. O leitor síncrono sincroniza o restante das saídas com o tempo de apresentação do quadro especificado do fluxo especificado.
2.  Comece a recuperar exemplos com chamadas para [**IWMSyncReader::GetNextSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) Continue como faria normalmente com o leitor síncrono.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o Leitor Síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Suporte a código de hora SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




