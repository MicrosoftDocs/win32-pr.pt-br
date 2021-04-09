---
description: Um reconhecedor pode encontrar várias maneiras de dividir uma amostra de tinta em segmentos de reconhecimento. Por isso, o número de alternativas de reconhecimento pode ser escalonado, mesmo para uma amostra de tinta pequena.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmentos de tinta e alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010465"
---
# <a name="ink-segments-and-alternates"></a>Segmentos de tinta e alternativas

Um reconhecedor pode encontrar várias maneiras de dividir uma amostra de tinta em segmentos de reconhecimento. Por isso, o número de alternativas de reconhecimento pode ser escalonado, mesmo para uma amostra de tinta pequena.

Por exemplo, "t o g e t h e r" podem produzir os seguintes resultados:

-   "para obter a sua" (além de alternativas para cada palavra)
-   "para reunir" (além de alternativas para cada palavra)
-   "Tog ether" (mais alternativas para cada palavra)
-   "Tog" (além de alternativas para cada palavra)
-   "juntos" (além de alternativas para a palavra)

O objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dá suporte ao armazenamento eficiente de resultados de reconhecimento completo no objeto [**Ink**](inkdisp-class.md) . O objeto de **tinta** mapeia as alternativas de reconhecimento para os traços no objeto de **tinta** e também pode conter outras informações, como posição da linha de base, índices de linha e intervalos de idiomas.

 

 



