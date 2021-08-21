---
title: Diretrizes de autor para arquivos MIDI
description: Diretrizes de autor para arquivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- MIDI (Instrument Digital Interface Instrument), diretrizes de produção de arquivo
- MIDI (Interface Digital do Instrument Instrument), diretrizes de produção de arquivo
- criando arquivos MIDI, diretrizes de criação de arquivos
- Atribuições de patch MIDI padrão
- Atribuições de chave MIDI padrão
- MIDI (Instrument Digital Interface Instrument), atribuições de patch padrão
- MIDI (Interface Digital do Instrument Instrument), atribuições de patch padrão
- MIDI (Instrument Digital Interface Instrument), atribuições de chave padrão
- MIDI (Interface Digital do Instrument Instrument), atribuições de chave padrão
- criando arquivos MIDI, atribuições de patch padrão
- criando arquivos MIDI, atribuições de chave padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065636"
---
# <a name="authoring-guidelines-for-midi-files"></a>Diretrizes de autor para arquivos MIDI

Siga estas diretrizes para a geração de arquivos MIDI independentes de dispositivo para Windows:

-   Use as [Atribuições de Patch MIDI](standard-midi-patch-assignments.md) Padrão e [As Atribuições de Chave MIDI Padrão.](standard-midi-key-assignments.md)
-   Sempre envie uma mensagem de alteração de programa para um canal para selecionar um patch antes de enviar outras mensagens para esse canal. Para os dois canais de canais (10 e 16), selecione o número do programa 0.
-   Sempre siga uma mensagem de alteração de programa MIDI com uma mensagem do controlador de volume principal MIDI (número do controlador 7) para definir o volume relativo do patch.
-   Use um valor de 80 (0x50) para o controlador de volume principal para níveis de escuta normais. Para níveis mais silenciosos ou mais altos, você pode usar valores inferiores ou mais altos.
-   Use apenas as seguintes mensagens MIDI: anotações com velocidade, anotações, alteração de programa, inclinação de inclinação, volume principal (controlador 7) e botão de navegação (controlador 64). Sintetizadores internos são necessários para responder a essas mensagens e a maioria dos instrumentos MIDI também responde a elas.

 

 




