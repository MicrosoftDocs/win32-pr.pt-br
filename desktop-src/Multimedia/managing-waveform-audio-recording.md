---
title: Gerenciando a gravação de Waveform-Audio
description: Gerenciando a gravação de Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- áudio de onda, gravação
- Wave-interface de áudio, gravação
- gravando áudio de onda, sobre
- Estrutura WAVEHDR
- função waveInAddBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293939"
---
# <a name="managing-waveform-audio-recording"></a>Gerenciando a gravação de Waveform-Audio

Depois de abrir um dispositivo de entrada de wave-áudio, você pode começar a gravar dados de formato de onda-áudio. Formato de onda-os dados de áudio são registrados em buffers fornecidos pelo aplicativo especificados por uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) . Esses blocos de dados devem ser preparados antes de serem usados; para obter mais informações, consulte [blocos de dados de áudio](audio-data-blocks.md).

O Windows fornece as seguintes funções para gerenciar a gravação de formato wave-áudio.



| Função                                   | Descrição                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Envia um buffer para o driver de dispositivo para que ele possa ser preenchido com dados gravados de onda de áudio. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Interrompe a gravação de wave-áudio e marca todos os buffers pendentes como concluído.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Inicia a onda-gravação de áudio.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Interrompe a gravação de wave-áudio.                                                            |



 

Use a função [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) para enviar buffers para o driver de dispositivo. Como os buffers são preenchidos com dados gravados de Wave-Audio, o aplicativo é notificado com uma mensagem de janela, mensagem de retorno de chamada, mensagem de thread ou evento, dependendo do sinalizador especificado quando o dispositivo foi aberto.

Antes de começar a gravar usando o [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), você deve enviar pelo menos um buffer para o driver ou os dados de entrada podem ser perdidos.

Antes de fechar o dispositivo usando [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), chame [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) para marcar os blocos de dados pendentes como sendo feitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 