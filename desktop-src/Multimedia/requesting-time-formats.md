---
title: Solicitando formatos de hora
description: Solicitando formatos de hora
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- MIDI (interface digital de instrumento musical), formatos de hora
- MIDI (interface digital de instrumentos musicais), formatos de hora
- Serviços de MIDI, formatos de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640476"
---
# <a name="requesting-time-formats"></a>Solicitando formatos de hora

O Windows usa a estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para representar o tempo em um ou mais formatos diferentes, incluindo formatos de ponteiro de música de milissegundos, exemplos, SMPTE e MIDI. O membro **wType** especifica o formato de hora.

A função [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) usa a estrutura **MMTIME** . Antes de chamar essa função, você deve definir o membro **wType** para indicar o formato de hora solicitado. Para ver se o formato de hora solicitado tem suporte, verifique **wType** após a chamada. Se o formato de hora solicitado não tiver suporte, a hora será especificada em um formato de hora alternativo selecionado pelo driver de dispositivo e o membro **wType** será alterado para indicar o formato de hora selecionado.

Para obter mais informações sobre a estrutura **MMTIME** , consulte [timers de multimídia](multimedia-timers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 