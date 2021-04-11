---
title: Reamostragem de áudio
description: Reamostragem de áudio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- SDK do Windows Media Format, reamostragem de áudio
- Windows Media Format SDK, reamostrando áudio
- Formato de sistema avançado (ASF), reamostragem de áudio
- ASF (formato de sistemas avançados), reamostragem de áudio
- ASF (Advanced Systems Format), resolução de áudio de reamostragem
- ASF (formato de sistemas avançados), áudio de reamostragem
- reamostragem de áudio
- reamostrando áudio, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292162"
---
# <a name="audio-resampling"></a>Reamostragem de áudio

Cada formato compactado de um codec de áudio tem uma taxa de amostragem e tamanho de amostra específicos. Eles não precisam corresponder às configurações do formato de entrada ou de saída. Se um formato de entrada tiver configurações diferentes do formato compactado descrito no perfil, o gravador recriará a amostra do áudio, durante o processo de codificação, para corresponder ao formato compactado. Somente determinados formatos são aceitos pelo gravador como entrada. Quando você enumera os formatos de entrada para um fluxo de áudio compactado, todos os formatos recuperados podem ser reamostrados para corresponder ao formato no perfil.

Ao ler áudio compactado, o leitor irá reamostrar o conteúdo para corresponder ao formato de saída. Você deve usar um dos formatos de saída enumerados pelo leitor, portanto, você tem a garantia de que o áudio pode ser reamostrado para as configurações de formato de saída.

Cada reamostrabilidade potencialmente afeta a qualidade do áudio. Quando possível, você deve usar formatos de entrada e saída com configurações que correspondam ao formato compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de gravação de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




