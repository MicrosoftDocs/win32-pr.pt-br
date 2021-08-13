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
ms.openlocfilehash: e218384b1a27bb3240ac74ad9af6d8298945bb57dfaf635531cb4cbb9aaa9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432609"
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

 

 




