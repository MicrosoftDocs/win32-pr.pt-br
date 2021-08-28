---
title: Conversão de espaço em cores
description: Conversão de espaço em cores
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows SDK de Formato de Mídia, conversão de espaço em cores
- ASF (Advanced Systems Format), conversão de espaço em cores
- ASF (Formato de Sistemas Avançados), conversão de espaço em cores
- conversão de espaço de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b596b7ae8ed32e64cc3ebe8a23f1bc52dafb5304308104aba083675afe6370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447936"
---
# <a name="color-space-conversion"></a>Conversão de espaço em cores

Geralmente, há uma diferença entre a profundidade de cor do formato de vídeo compactado no perfil e o formato de entrada. Quando isso acontece, o vídeo de origem deve ser convertido para estar em conformidade com o espaço de cores do destino. O autor lida com esse processo, comunicando-se com um conversor interno de espaço de cores.

O leitor também se comunica com o conversor de espaço de cor para reconciliar qualquer diferença entre o formato compactado e o formato de saída.

Assim como com todas as transformação executadas nos dados, a conversão entre profundidades de cor pode reduzir a qualidade da saída. Quando possível, você deve usar formatos de entrada e saída com a mesma profundidade de cor que o formato compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de escrita de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




