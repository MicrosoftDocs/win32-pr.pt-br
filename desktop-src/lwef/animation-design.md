---
title: Design de animação
description: Design de animação
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225a500d94b4de6f9133650a6aed415a49329585bc9bc9f83dec028668e51215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752287"
---
# <a name="animation-design"></a>Design de animação

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="image-design"></a>Design de imagem

Use a Microsoft Office paleta ao projetar seus caracteres para minimizar possíveis problemas de realização da paleta. Evite selecionar uma cor de transparência semelhante às cores que você usa em seu documento.

### <a name="sounds"></a>Sons

O Microsoft Agent permite que você reproduza sons em suas animações. Recomendamos que você não inclua sons para suas **animações** Ociosas. Isso é para que não haja um atraso no meio da animação, se o Agent tiver que carregar a DLL multimídia do sistema.

### <a name="frame-size"></a>Tamanho do quadro

As Office assistentes comuns têm 123 x 93 pixels. Embora você possa criar caracteres de outros tamanhos, eles serão dimensionados para 123 x 93 na Galeria do Assistente.

### <a name="frame-transition"></a>Transição de quadro

Todas as animações, exceto **Até Logo,** **Saudação**, **Mostrar** e **Ocultar** devem começar e terminar com a animação RestPose. Microsoft Office não reproduz animações **de Retorno** explícitas, portanto, você não deve defini-las. Todas as animações também devem ter Ramificação de Saída. A ramificação de saída nos permite 'se manter e concluir' a animação atual antes de chamarmos a próxima animação. Se você não fornecer Ramificação de Saída, a transição entre animações poderá ser tranquila.

### <a name="character-properties"></a>Propriedades de caractere

O Microsoft Agent permite definir as propriedades [**Nome,**](name-property.md) [**Descrição**](description-property.md) e [**ExtraData**](extradata-property.md) do caractere. Microsoft Office usa o **campo ExtraData** para conter uma ou mais Frases de Introdução e Frases de Lembrete. Microsoft Office escolhe entre as outras Frases de Introdução para colocar no balão de fala na Galeria do Assistente. Usamos as Frases de Lembrete quando você recebe um lembrete Outlook.

O [**campo ExtraData**](extradata-property.md) é formatado da seguinte forma:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

As frases intro são separadas por um par de caracteres de til (~), seguidas por Frases de Lembrete. Essas Frases de Lembrete também são separadas por um par de caracteres de til. Os dois conjuntos de frases são separados por dois caracteres de (^^). Não há nenhum limite para o número de cada tipo de frase, exceto que deve haver pelo menos um de cada.

 

 




