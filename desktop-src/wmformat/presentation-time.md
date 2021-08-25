---
title: Tempo da apresentação
description: Tempo da apresentação
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows SDK de Formato de Mídia, tempos de apresentação
- ASF (Advanced Systems Format), tempos de apresentação
- ASF (Formato de Sistemas Avançados), tempos de apresentação
- tempos de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2dea9181552b42508745b256768b2c5ceb4443a057fc5d7d7a5a44410c788fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807906"
---
# <a name="presentation-time"></a>Tempo da apresentação

Um tempo de apresentação é uma medida de tempo da primeira amostra do primeiro fluxo em um arquivo ASF. Essa medida, bem como a maioria das outras medidas de tempo usadas pelos objetos desse SDK, está em unidades de 100 nanossegundos. Os tempos de apresentação são importantes porque permitem que os vários fluxos em um arquivo sejam sincronizados. Você deve fornecer um tempo de apresentação para cada exemplo de entrada que passar para o autor. Cada objeto de dados na seção de dados de um arquivo ASF tem um tempo de apresentação associado a ele. Cada exemplo de saída recuperado pelo leitor também tem um tempo de apresentação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Exemplos de mídia**](media-samples.md)
</dt> </dl>

 

 




