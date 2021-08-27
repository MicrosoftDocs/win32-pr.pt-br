---
title: Para buscar pelo código de tempo SMPTE usando o leitor assíncrono
description: Para buscar pelo código de tempo SMPTE usando o leitor assíncrono
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Formato de sistemas avançados (ASF), buscando por códigos de tempo SMPTE
- ASF (formato de sistemas avançados), buscando por códigos de tempo SMPTE
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- leitores assíncronos, buscando por códigos de tempo SMPTE
- leitores assíncronos, códigos de tempo SMPTE
- Códigos de tempo SMPTE, buscando
- Códigos de tempo SMPTE, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01ad42170c2458a4dc23a23cfa8102b406f45b6a624cacac28ce31a905ad299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110116"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>Para buscar pelo código de tempo SMPTE usando o leitor assíncrono

O objeto leitor pode buscar um ponto em um arquivo com base no código de tempo SMPTE associado a um fluxo de vídeo. Os dados de código de tempo são encapsulados em estruturas de dados de extensão do código de WMT que são anexadas a amostras de vídeo como extensões de unidade de dados. [**\_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)

Os códigos de tempo SMPTE são definidos por um intervalo e um código de tempo dentro desse intervalo. Um intervalo é uma série contínua de códigos de tempo. Cada código de tempo é definido por horas, minutos, segundos e quadros.

Para buscar dados em um arquivo ASF pelo código de tempo SMPTE usando o leitor assíncrono, execute as etapas a seguir.

1.  Obtenha um ponteiro para a interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) do objeto leitor chamando **IWMReader:: QueryInterface**.
2.  Defina o código e a duração da hora de início chamando [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Você deve especificar o número de fluxo de um fluxo de vídeo que é indexado por código de tempo. O leitor sincronizará o restante das saídas com o tempo de apresentação do quadro especificado do fluxo especificado e começará a fornecer amostras de saída.
3.  Manipule os exemplos como faria normalmente em sua implementação do método **IWMReaderCallback:: onsample** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> <dt>

[**Suporte ao código de tempo SMPTE**](smpte-time-code-support.md)
</dt> </dl>

 

 




