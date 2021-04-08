---
description: O terminal de reprodução de arquivos e a gravação de arquivos exibem as interfaces ITTerminal e ITMultiTrackTerminal. Esses objetos também expõem a interface ITMediaControl, que fornece métodos para parar, iniciar e navegar por mídia.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de reprodução de arquivos de terminal e gravação de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921697"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal de reprodução de arquivos de terminal e gravação de arquivos

O terminal de reprodução de arquivos e a gravação de arquivos exibem as interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) e [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) . Esses objetos também expõem a interface [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , que fornece métodos para parar, iniciar e navegar por mídia.

O terminal de reprodução de arquivo expõe a interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , que tem métodos específicos de reprodução.

O terminal de gravação de arquivo expõe a interface [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , que fornece métodos específicos de gravação.

Como [terminais multitrack](multitrack-terminals.md), o terminal de gravação de arquivos e terminal de reprodução de arquivos gerenciam uma coleção de [terminais de faixa](track-terminals.md).

 

 
