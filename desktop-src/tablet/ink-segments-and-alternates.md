---
description: Um reconhecedor pode encontrar várias maneiras de quebrar uma amostra de tinta em segmentos de reconhecimento. Por isso, o número de alternativas de reconhecimento pode ser escalonável, mesmo para uma amostra de tinta pequena.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmentos de tinta e alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c2da4984afd22490827acdf65962abc789d7ad9f0ddab3e602bc688ac6542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883986"
---
# <a name="ink-segments-and-alternates"></a>Segmentos de tinta e alternativas

Um reconhecedor pode encontrar várias maneiras de quebrar uma amostra de tinta em segmentos de reconhecimento. Por isso, o número de alternativas de reconhecimento pode ser escalonável, mesmo para uma amostra de tinta pequena.

Por exemplo, "t o g e t h e r" pode gerar os seguintes resultados:

-   "para obter a ela" (além de alternativas para cada palavra)
-   "para coletar" (mais alternativas para cada palavra)
-   "tog ether" (mais alternativas para cada palavra)
-   "tog at her" (além de alternativas para cada palavra)
-   "together" (mais alternativas para a palavra)

O [**objeto RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dá suporte ao armazenamento eficiente de resultados de reconhecimento completo dentro do [**objeto Ink.**](inkdisp-class.md) O **objeto Ink** mapeia as alternativas de reconhecimento para os traços no objeto **Ink** e também pode conter outras informações, como posição de linha de base, índices de linha e intervalos de idiomas.

 

 



