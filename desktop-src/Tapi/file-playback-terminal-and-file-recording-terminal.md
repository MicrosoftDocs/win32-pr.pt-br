---
description: O terminal de reprodução de arquivos e a gravação de arquivos exibem as interfaces ITTerminal e ITMultiTrackTerminal. Esses objetos também expõem a interface ITMediaControl, que fornece métodos para parar, iniciar e navegar por mídia.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de reprodução de arquivos de terminal e gravação de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad07ea46e2abf13465ac3344e69f586673c3b29463eac8bdd324966fb838368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100586"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal de reprodução de arquivos de terminal e gravação de arquivos

O terminal de reprodução de arquivos e a gravação de arquivos exibem as interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) e [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) . Esses objetos também expõem a interface [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , que fornece métodos para parar, iniciar e navegar por mídia.

O terminal de reprodução de arquivo expõe a interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , que tem métodos específicos de reprodução.

O terminal de gravação de arquivo expõe a interface [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , que fornece métodos específicos de gravação.

Como [terminais multitrack](multitrack-terminals.md), o terminal de gravação de arquivos e terminal de reprodução de arquivos gerenciam uma coleção de [terminais de faixa](track-terminals.md).

 

 
