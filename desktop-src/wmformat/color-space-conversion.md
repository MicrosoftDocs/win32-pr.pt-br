---
title: Conversão de espaço de cor
description: Conversão de espaço de cor
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- SDK do Windows Media Format, conversão de espaço em cores
- Formato de sistema avançado (ASF), conversão de espaço de cor
- ASF (formato de sistemas avançados), conversão de espaço de cor
- conversão de espaço de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159803"
---
# <a name="color-space-conversion"></a>Conversão de espaço de cor

Geralmente, há uma diferença entre a intensidade da cor do formato de vídeo compactado no perfil e o formato de entrada. Quando isso acontece, o vídeo de origem deve ser convertido para estar de acordo com o espaço de cores do destino. O gravador manipula esse processo, comunicando-se com um conversor de espaço de cor interno.

O leitor também se comunica com o conversor de espaço de cor para reconciliar qualquer diferença entre o formato compactado e o formato de saída.

Assim como todas as transformações executadas nos dados, a conversão entre as profundidades de cor pode reduzir a qualidade da saída. Quando possível, você deve usar formatos de entrada e saída com a mesma intensidade de cor que o formato compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de gravação de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




