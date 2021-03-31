---
title: Suporte ao balão do Word
description: Suporte ao balão do Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159576"
---
# <a name="word-balloon-support"></a>Suporte ao balão do Word

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A saída falada também pode aparecer como saída textual na forma de um balão de palavras de desenho. Isso pode ser usado para complementar a saída falada de um caractere ou como uma alternativa à saída de áudio quando você usa o método [**Speak**](speak-method.md) .

![Sim balão de palavras mestras](images/f3ballon.gif)

Você também pode usar um balão de palavra para comunicar o que um caractere está "pensando" usando o método [**Think**](think-method.md) . Isso exibe o texto que você fornece em um balão ainda "pensado". O método **Think** também difere do método [**Speak**](speak-method.md) , pois ele não produz nenhuma saída de áudio.

Os balões de palavras dão suporte apenas à comunicação com legendas do caractere, não à entrada do usuário. Portanto, o balão de palavras não dá suporte a controles de entrada. No entanto, você pode fornecer facilmente a entrada do usuário para um caractere, usando interfaces da linguagem de programação ou outros serviços de entrada fornecidos pelo Microsoft Agent, como o menu pop-up.

Ao definir um caractere, você pode especificar se deseja incluir o suporte ao balão do Word. No entanto, se você usar um caractere que inclua suporte a balão de palavras, não será possível desabilitar o suporte.

 

 




