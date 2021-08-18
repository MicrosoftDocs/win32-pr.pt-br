---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de27451826a232092bc74e630a54621a004cc15e44ad4a9a7d3377509ff00ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476713"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O mecanismo deve chamar por meio **de BookMark**. Durante o pré-processamento da saída de fala, o código do Microsoft Agent insere indicadores entre "palavras" e usa a chegada desses indicadores para impulsionar o espaçamento do texto no balão de palavras. Embora o SAPI não exige nada mais do que a chegada desses indicadores em algum momento antes do término do enunciado, os indicadores devem ser retornados de forma relativamente o tempo hábil para dar suporte ao Microsoft Agent.

Observe que não há nenhum conceito estrito de "palavra" em alguns idiomas, como japonês. O método [**Speak**](speak-method.md) do Microsoft Agent define uma "palavra" como uma cadeia de caracteres conectada de símbolos que tem um significado e uma pronúncia isoladas. O Microsoft Agent usa um código de análise bastante simples para determinar o que é uma "palavra": ele procura símbolos separados por espaço em branco. Portanto, há três "palavras" na cadeia de caracteres em inglês "The 101 Dalmacians": "the", "one hundred and one" e "Dalmacians". O texto incluído na marca de Mapa do Microsoft Agent é tratado como uma única "palavra" para fins de exibição.

 

 




