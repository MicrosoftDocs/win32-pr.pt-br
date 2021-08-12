---
title: Usando a interface IWMPCdromRip
description: Usando a interface IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, CD
- Windows Media Player modelo de objeto, CD
- modelo de objeto, CD
- Windows Media Player ActiveX controle,CD
- ActiveX controle,CD
- Windows Media Player Controle ActiveX dispositivo móvel, CD
- Windows Media Player Móvel, CD
- CD ,interface IWMPCdromRip
- CDs de máquina, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50651629f5a11f13bb27a11927c1f08c33de7162130fd7f10f33fe4c74386692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569792"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Usando a interface IWMPCdromRip

Esta seção descreve como usar a interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para cortar música de um CD.

A replicação de um CD usando a interface **IWMPCdromRip** tem o mesmo efeito que a música de voz ao usar a interface do Windows Media Player usuário. O conteúdo da biblioteca é adicionado automaticamente à biblioteca de acordo com as preferências do usuário. Para obter mais informações sobre a gravação de CD, consulte "Música de música de música de CDs" em Windows Media Player Ajuda.

Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.

## <a name="included-headers"></a>Headers incluídos

Para usar o código nesta seção, inclua os seguintes headers:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>Ponteiros de interface

As interfaces para Windows Media Player são armazenadas nas seguintes variáveis de membro.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



As seções a seguir descrevem como usar a interface IWMPCdromRip

-   [Recuperar a interface de extração](retrieving-the-ripping-interface.md)
-   [Iniciando o processo de ressarção](starting-the-rip-process.md)
-   [Recuperando o status de resserção](retrieving-the-rip-status.md)
-   [Selecionando itens para Busca](selecting-items-for-ripping.md)

 

 




