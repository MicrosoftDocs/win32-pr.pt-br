---
title: Formato de buffer de fluxo
description: Formato de buffer de fluxo
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- buffers de fluxo, formato
- Estrutura MIDIHDR
- Estrutura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072c2541ab6b731686fc63c59b11b0dfff529ef9cab347d41fbddf13e9b60b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688496"
---
# <a name="stream-buffer-format"></a>Formato de buffer de fluxo

O membro **lpData** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) aponta para um buffer de fluxo e o membro **dwBufferLength** especifica o tamanho real desse buffer. O membro **dwBytesRecorded** de **MIDIHDR** especifica o número de bytes no buffer que são realmente usados pelos eventos de Midi; Esse valor deve ser menor ou igual ao valor especificado por **dwBufferLength**.

Cada um dos eventos de MIDI no buffer de fluxo é especificado por uma estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , que contém a hora do evento, um identificador de fluxo, um código de evento e, quando apropriado, os parâmetros para o evento. Cada uma dessas estruturas **MIDIEVENT** deve começar em um limite de doubleword. Se necessário, os bytes de preenchimento devem ser adicionados ao final da estrutura para garantir que o próximo seja iniciado em um limite de doubleword.

 

 