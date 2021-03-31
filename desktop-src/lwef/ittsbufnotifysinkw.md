---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916574"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O mecanismo deve chamar o **indicador**. Durante o pré-processamento da saída de fala, o código do Microsoft Agent insere indicadores entre "palavras" e usa a chegada desses indicadores para impulsionar o ritmo do texto na palavra balão. Embora SAPI não exija nada mais do que a chegada desses indicadores em algum momento antes do final do expressão, os indicadores devem ser retornados de forma relativamente oportuna para dar suporte ao Microsoft Agent.

Observe que não há um conceito estrito de "Word" em algumas linguagens, como o japonês. O método [**Speak**](speak-method.md) do Microsoft Agent define uma "palavra" como uma cadeia de caracteres conectada de símbolos que tem um significado e uma pronúncia isoladamente. O Microsoft Agent usa um código de análise bastante simples para determinar o que é uma "palavra": ele procura símbolos separados por espaço em branco. Portanto, há três "palavras" na cadeia de caracteres em inglês "The 101 Dalmatians": "," 101 "e" Dalmatians ". O texto incluído na marca de mapa do Microsoft Agent é tratado como uma única "palavra" para fins de exibição.

 

 




