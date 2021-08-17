---
title: Reamostragem de áudio
description: Reamostragem de áudio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows SDK de formato de mídia, reamostragem de áudio
- Windows SDK de formato de mídia, reamostrando áudio
- Formato de sistema avançado (ASF), reamostragem de áudio
- ASF (formato de sistemas avançados), reamostragem de áudio
- ASF (Advanced Systems Format), resolução de áudio de reamostragem
- ASF (formato de sistemas avançados), áudio de reamostragem
- reamostragem de áudio
- reamostrando áudio, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5d95ed50117ac9d0fe7d71a2148314e1b9faf3ba8a26b99bb69083029b991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434470"
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

 

 




