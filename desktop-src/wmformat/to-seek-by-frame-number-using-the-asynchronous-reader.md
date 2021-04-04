---
title: Para buscar por número de quadro usando o leitor assíncrono
description: Para buscar por número de quadro usando o leitor assíncrono
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- ASF (Advanced Systems Format), buscando por números de quadro
- ASF (formato de sistemas avançados), busca por números de quadro
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, procurando por números de quadro
- fluxos de vídeo, buscando por números de quadro
- fluxos de vídeo, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007095"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Para buscar por número de quadro usando o leitor assíncrono

O objeto leitor assíncrono pode ser usado para buscar os números de quadro de fluxos de vídeo em um arquivo ASF. Para usar a busca baseada em quadros, o arquivo carregado no leitor deve ser indexado por quadro. Cada fluxo de vídeo individual pode ser indexado. Para determinar se um fluxo foi indexado por frame, você pode verificar o \_ atributo g wszWMNumberOfFrames no cabeçalho do arquivo chamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar dados em um arquivo ASF por número de quadro usando o leitor assíncrono, execute as etapas a seguir.

1.  Obtenha um ponteiro para a interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) do objeto leitor chamando **IWMReader:: QueryInterface**.
2.  Defina o número do quadro inicial e a duração chamando [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Você deve especificar o número de fluxo de um fluxo de vídeo indexado por quadro. O leitor sincronizará o restante das saídas com o tempo de apresentação do quadro especificado do fluxo especificado e começará a fornecer amostras de saída.
3.  Manipule os exemplos como faria normalmente em sua implementação do método **IWMReaderCallback:: onsample** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lendo metadados na reprodução**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




