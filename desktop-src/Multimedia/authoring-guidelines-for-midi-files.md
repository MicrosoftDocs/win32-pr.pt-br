---
title: Diretrizes de criação para arquivos MIDI
description: Diretrizes de criação para arquivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- MIDI (interface digital de instrumento musical), diretrizes de criação de arquivo
- A MIDI (interface digital de instrumentos musicais), diretrizes de criação de arquivo
- Criando arquivos MIDI, diretrizes de criação de arquivo
- atribuições de patch de MIDI padrão
- atribuições de chave MIDI padrão
- MIDI (interface digital de instrumento musical), atribuições de patch padrão
- MIDI (interface digital de instrumentos musicais), atribuições de patch padrão
- MIDI (interface digital de instrumento musical), atribuições de chave padrão
- MIDI (interface digital de instrumentos musicais), atribuições de chave padrão
- Criando arquivos MIDI, atribuições de patch padrão
- Criando arquivos MIDI, atribuições de chave padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006075"
---
# <a name="authoring-guidelines-for-midi-files"></a>Diretrizes de criação para arquivos MIDI

Siga estas diretrizes para criar arquivos MIDI independentes de dispositivo para o Windows:

-   Use as atribuições de [patch de Midi padrão](standard-midi-patch-assignments.md) e as [atribuições de chave MIDI padrão](standard-midi-key-assignments.md).
-   Sempre envie uma mensagem de alteração de programa a um canal para selecionar um patch antes de enviar outras mensagens para esse canal. Para os dois canais de percussão (10 e 16), selecione o número do programa 0.
-   Sempre siga um programa MIDI-alterar mensagem com uma mensagem MIDI principal-controlador de volume (número do controlador 7) para definir o volume relativo do patch.
-   Use um valor de 80 (0x50) para o controlador de volume principal para os níveis de escuta normais. Para níveis mais silenciosos ou mais altos, você pode usar valores menores ou mais altos.
-   Use apenas as seguintes mensagens de MIDI: observação-em com velocidade, anotação, alteração de programa, curva de densidade, volume principal (controlador 7) e pedal de amortecedor (controlador 64). Os sintetizadores internos são necessários para responder a essas mensagens e a maioria dos instrumentos musicais MIDI também responde a elas.

 

 




