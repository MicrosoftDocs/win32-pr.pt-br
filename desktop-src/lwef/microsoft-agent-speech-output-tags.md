---
title: Marcas de saída de fala do Microsoft Agent
description: Marcas de saída de fala do Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27add35cc9be72a002cdb1a6fba60ef61d47cca61ef532a6d80fd6ed4a5794d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747863"
---
# <a name="microsoft-agent-speech-output-tags"></a>Marcas de saída de fala do Microsoft Agent

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os serviços do Microsoft Agent dão suporte à modificação da saída de fala por meio de marcas especiais inseridas na cadeia de texto de fala. Essas marcas ajudam a alterar as características da expressão de saída do caractere.

As marcas de saída de fala usam as seguintes regras de sintaxe:

-   Todas as marcas começam e terminam com um caractere de barra invertida ( \\ ).
-   O caractere de barra invertida simples não está habilitado dentro de uma marca. Para incluir um caractere de barra invertida em um parâmetro de texto de uma marca, use uma barra invertida dupla ( \\ \\ ).
-   As marcas não diferenciam maiúsculas de minúsculas. Por exemplo, \\ \\ o Pit é o mesmo que o \\ Pit \\ .
-   As marcas são dependentes de espaço em branco. Por exemplo, \\ RST \\ não é o mesmo que \\ RST \\ .

A menos que especificado em contrário ou modificado por outra marca, a saída de fala retém a característica definida pela marca dentro do texto especificado em um único método de [**fala**](speak-method.md) . A saída de fala é redefinida automaticamente por meio dos parâmetros definidos pelo usuário depois que um método de **fala** é concluído.

Algumas marcas incluem cadeias de caracteres entre aspas. para algumas linguagens de programação, como o Visual Basic scripting Edition (VBScript) e Visual Basic, isso significa que você pode precisar usar duas aspas para designar o parâmetro da marca ou concatenar um caractere de aspas duplas como parte da cadeia de caracteres. o último é mostrado neste Visual Basic exemplo:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Para C, C++ e Java™ programação, preceda as barras invertidas e aspas duplas com uma barra invertida. Por exemplo:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Para idiomas estrangeiros que dão suporte a caracteres DBCS (conjunto de caracteres de dois bytes), você pode usar caracteres de byte duplo para especificar parâmetros de cadeia de caracteres. No entanto, use caracteres de byte único para todos os outros parâmetros e caracteres que são usados para definir a marca, incluindo a marca em si.

Há suporte para as seguintes marcas:

-   [**Chr**](chr-tag.md)
-   [**CTX**](ctx-tag.md)
-   [**EMP**](emp-tag.md)
-   [**Ficheiro**](lst-tag.md)
-   [**Mapeamento**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Poço**](pit-tag.md)
-   [**RST**](rst-tag.md)
-   [**SPD**](spd-tag.md)
-   [**Vol**](vol-tag.md)

As marcas são projetadas principalmente para ajustar a saída gerada por conversão de texto em fala (TTS). Somente as marcas [**mrk**](mrk-tag.md) e [**MAP**](map-tag.md) podem ser usadas com saída falada com base em arquivo de som.

> [!Note]  
> O Microsoft Agent não oferece suporte a todas as marcas documentadas no SDK do Microsoft Speech. Os parâmetros também podem variar dependendo do mecanismo de TTS selecionado. Você pode definir um mecanismo de TTS específico usando [**TTSModeID**](ttsmodeid-property.md).

 

 

 




