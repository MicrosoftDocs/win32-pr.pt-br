---
title: Tempo da apresentação
description: Tempo da apresentação
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- SDK do Windows Media Format, tempos de apresentação
- ASF (Advanced Systems Format), tempos de apresentação
- ASF (formato de sistemas avançados), tempos de apresentação
- tempos de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292616"
---
# <a name="presentation-time"></a>Tempo da apresentação

Um tempo de apresentação é uma medida de tempo desde a primeira amostra do primeiro fluxo em um arquivo ASF. Essa medida, bem como a maioria das outras medições de tempo usada pelos objetos desse SDK, está em unidades de 100 nanossegundos. Os tempos de apresentação são importantes porque permitem que os vários fluxos em um arquivo sejam sincronizados. Você deve fornecer um tempo de apresentação para cada exemplo de entrada que passa para o gravador. Cada objeto de dados na seção de dados de um arquivo ASF tem um tempo de apresentação associado a ele. Cada exemplo de saída recuperada pelo leitor também tem um tempo de apresentação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Entradas, fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Amostras de mídia**](media-samples.md)
</dt> </dl>

 

 




