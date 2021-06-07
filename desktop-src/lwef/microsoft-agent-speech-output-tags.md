---
title: Marcas de saída de fala do Microsoft Agent
description: Marcas de saída de fala do Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386795"
---
# <a name="microsoft-agent-speech-output-tags"></a>Marcas de saída de fala do Microsoft Agent

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os serviços do Microsoft Agent suportam a modificação da saída de fala por meio de marcas especiais inseridas na cadeia de caracteres de texto de fala. Essas marcas ajudam você a alterar as características da expressão de saída do caractere.

As marcas de saída de fala usam as seguintes regras de sintaxe:

-   Todas as marcas começam e terminam com um caractere de faixa invertida ( \\ ).
-   O caractere de faixa invertida única não está habilitado em uma marca. Para incluir um caractere de faixa invertida em um parâmetro de texto de uma marca, use uma faixa invertida dupla ( \\ \\ ).
-   As marcas não são sensíveis a maiúsculas e minúsculas. Por exemplo, \\ pit é o mesmo que PIT \\ \\ \\ .
-   As marcas são dependentes de espaço em branco. Por exemplo, \\ Rst \\ não é o mesmo que \\ Rst \\ .

A menos que especificado ou modificado de outra marca, a saída de fala retém a característica definida pela marca dentro do texto especificado em um único [**método Speak.**](speak-method.md) A saída de fala é redefinida automaticamente por meio dos parâmetros definidos pelo usuário depois que um **método Speak** é concluído.

Algumas marcas incluem cadeias de caracteres entre aspas. Para algumas linguagens de programação, como Visual Basic Scripting Edition (VBScript) e Visual Basic, isso significa que você pode ter que usar duas aspas para designar o parâmetro da marca ou concatenar um caractere de aspas duplas como parte da cadeia de caracteres. O último é mostrado neste Visual Basic exemplo:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Para programação C, C++e Java™, preceda aspas invertida e aspas duplas com uma faixa invertida. Por exemplo:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Para linguagens estrangeiras que suportam caracteres DBCS (conjunto de caracteres de byte duplo), você pode usar caracteres de byte duplo para especificar parâmetros de cadeia de caracteres. No entanto, use caracteres de byte único para todos os outros parâmetros e caracteres usados para definir a marca, incluindo a marca em si.

Há suporte para as seguintes marcas:

-   [**Chr**](chr-tag.md)
-   [**Ctx**](ctx-tag.md)
-   [**Emp**](emp-tag.md)
-   [**Lst**](lst-tag.md)
-   [**Mapa**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Poço**](pit-tag.md)
-   [**Rst**](rst-tag.md)
-   [**Spd**](spd-tag.md)
-   [**Vol**](vol-tag.md)

As marcas são projetadas principalmente para ajustar a saída gerada por TTS (texto em fala). Somente as [**marcas Mrk**](mrk-tag.md) e [**Map**](map-tag.md) podem ser usadas com saída falada baseada em arquivo de som.

> [!Note]  
> O Microsoft Agent não dá suporte a todas as marcas documentadas no SDK de Fala da Microsoft. Os parâmetros também podem variar dependendo do mecanismo TTS selecionado. Você pode definir um mecanismo TTS específico usando [**TTSModeID.**](ttsmodeid-property.md)

 

 

 




