---
description: A lista a seguir contém os membros do CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Membros do CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091656"
---
# <a name="cmspstream-members"></a>Membros do CMSPStream



| Tipo de membro                     | Nome                | Descrição                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*\_pFTM m           | Ponteiro para o Marshaller com thread livre.                                                                                                   |
| DWORD                           | \_dwState m          | O estado atual do fluxo.                                                                                                           |
| PROCESSAMENTO                          | \_hAddress m         | O endereço no qual esse fluxo está sendo usado.                                                                                            |
| DWORD                           | \_dwMediaType m      | O [**tipo de mídia**](tapimediatype--constants.md) desse fluxo (áudio, vídeo, etc.).                                                    |
| direção do TERMINAL \_             | \_direção m        | A [**direção**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) desse fluxo (entrada ou saída).                                                         |
| CMSPCallBase                    | \*\_pMSPCall m       | Ponteiro para o objeto de chamada.                                                                                                                |
| IGraphBuilder                   | \*\_pIGraphBuilder m | Ponteiro para interfaces de objeto de gráfico.                                                                                                        |
| IMediaControl                   | \*\_pIMediaControl m | Ponteiro para a interface de controle de mídia.                                                                                                    |
| CMSPArray <ITTerminal \*> | \_terminais m        | A lista de terminais no fluxo.                                                                                                       |
| CMSPCritSection                 | bloqueio de m \_             | O bloqueio que protege o objeto de fluxo. O objeto Stream nunca deve adquirir o bloqueio e, em seguida, chamar um método MSPCall que possa ser bloqueado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



