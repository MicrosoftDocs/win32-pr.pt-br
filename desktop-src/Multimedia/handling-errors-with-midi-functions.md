---
title: Tratamento de erros com funções MIDI
description: Tratamento de erros com funções MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- MIDI (interface digital de instrumento musical), erros
- MIDI (interface digital de instrumentos musicais), erros
- Serviços MIDI, erros
- Erros de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105748131"
---
# <a name="handling-errors-with-midi-functions"></a>Tratamento de erros com funções MIDI

As funções de áudio MIDI retornam um código de erro diferente de zero. Para erros associados a MIDI, as funções [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) e [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperam descrições textuais para os códigos de erro. O aplicativo ainda deve examinar o valor do erro em si para determinar como proceder, mas pode usar as descrições de erro nas caixas de diálogo para informar os usuários sobre as condições de erro.

As únicas funções de MIDI que não retornam códigos de erro são as funções [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) e [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Essas funções retornarão um valor de zero se nenhum dispositivo estiver presente em um sistema ou se algum erro for encontrado pela função.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 