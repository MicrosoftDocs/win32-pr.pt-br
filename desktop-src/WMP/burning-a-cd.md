---
title: Gravar um CD
description: Gravar um CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, gravação de CD
- Windows Media Player modelo de objeto, gravação de CD
- modelo de objeto, gravação de CD
- Windows Media Player ActiveX controle, gravação de CD
- ActiveX controle, gravação de CD
- Windows Media Player Controle de ActiveX móvel, gravação de CD
- Windows Media Player Móvel, gravação de CD
- Gravação de CD, sobre
- CDs de gravação, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c7cfee7468b2cd376b7b25d4cff4a04e0d057dcc7a792ac7471843de2b74a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840765"
---
# <a name="burning-a-cd"></a>Gravar um CD

Esta seção descreve como usar a interface [IWMPCdrom Ltda](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) para gravar música em um CD. A interface **IWMPCdrom Ltda** fornece funcionalidade para playlists de gravação para CDs como faixas de áudio ou dados, bem como para apagar CD-RWs.

Uso de código

Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.

Headers incluídos

Para usar o código nesta seção, inclua os seguintes headers:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Ponteiros de interface

As interfaces para Windows Media Player são armazenadas nas seguintes variáveis de membro:


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



Os tópicos a seguir descrevem como usar a API de gravação de CD.

-   [Recuperar a interface de gravação de CD](retrieving-the-cd-burning-interface.md)
-   [Iniciando o processo de burn](starting-the-burn-process.md)
-   [Apagando um CD reeritável](erasing-a-rewritable-cd.md)
-   [Recuperando o status da unidade e do disco](retrieving-the-drive-and-disc-status.md)
-   [Recuperando o status de burn](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de controle do player**](player-control-guide.md)
</dt> </dl>

 

 




