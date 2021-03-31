---
title: Design de animação
description: Design de animação
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916153"
---
# <a name="animation-design"></a>Design de animação

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="image-design"></a>Design de imagem

Use a paleta de Microsoft Office ao criar seus caracteres para minimizar possíveis problemas de realização de paleta. Evite selecionar uma cor de transparência que seja semelhante às cores que você usa em seu documento.

### <a name="sounds"></a>Sons

O Microsoft Agent permite que você jogue sons em suas animações. Recomendamos que você não inclua sons para suas animações **ociosas** . Isso é assim, não haverá um atraso no meio da animação, se o Agent tiver que carregar a DLL de multimídia do sistema.

### <a name="frame-size"></a>Tamanho do quadro

Os assistentes típicos do Office são 123 x 93 pixels. Embora você possa criar caracteres de outros tamanhos, eles serão dimensionados para 123 x 93 na galeria do assistente.

### <a name="frame-transition"></a>Transição de quadros

Todas as animações, exceto para **adeus**, **saudação**, **Mostrar** e **ocultar** , devem começar e terminar com a animação RestPose. Microsoft Office não reproduz animações de **retorno** explícitas, portanto, você não deve defini-las. Todas as animações também devem ter ramificações de saída. Sair da ramificação nos permite ' ressaltar e concluir ' a animação atual antes de chamarmos a próxima animação. Se você não fornecer a ramificação de saída, a transição entre animações pode ser jerky.

### <a name="character-properties"></a>Propriedades de caractere

O Microsoft Agent permite que você defina as propriedades [**Name**](name-property.md), [**Description**](description-property.md) e [**ExtraData**](extradata-property.md) do caractere. Microsoft Office usa o campo **ExtraData** para armazenar uma ou mais frases de introdução e frases de lembrete. Microsoft Office escolhe das outras frases de introdução para colocar no balão de fala na galeria do assistente. Usamos as frases de lembrete quando você recebe um lembrete do Outlook.

O campo [**ExtraData**](extradata-property.md) é formatado da seguinte maneira:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

As frases de introdução são separadas por um par de caracteres de til (~), seguidos por frases de lembrete. Essas frases de lembrete também são separadas por um par de caracteres de til. Os dois conjuntos de frases são separados por dois caracteres de cursor (^^). Não há nenhum limite para o número de cada tipo de frase, exceto pelo fato de que deve haver pelo menos um de cada.

 

 




