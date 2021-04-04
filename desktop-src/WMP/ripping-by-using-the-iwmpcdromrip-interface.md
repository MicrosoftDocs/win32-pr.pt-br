---
title: Copiando usando a interface IWMPCdromRip
description: Copiando usando a interface IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, interface IWMPCdromRip
- copiando CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823572"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Copiando usando a interface IWMPCdromRip

Esta seção descreve como usar a interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para copiar música de um CD.

Copiar um CD usando a interface **IWMPCdromRip** tem o mesmo efeito que copiar música usando a interface do usuário do Windows Media Player. O conteúdo copiado é adicionado automaticamente à biblioteca de acordo com as preferências do usuário. Para obter mais informações sobre cópia de CD, consulte "copiando música de CDs" na ajuda do Windows Media Player.

Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.

## <a name="included-headers"></a>Cabeçalhos incluídos

Para usar o código nesta seção, inclua os seguintes cabeçalhos:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>Ponteiros de interface

As interfaces do Windows Media Player são armazenadas nas seguintes variáveis de membro.


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
-   [Iniciando o processo de RIP](starting-the-rip-process.md)
-   [Recuperando o status do RIP](retrieving-the-rip-status.md)
-   [Selecionando itens para copiar](selecting-items-for-ripping.md)

 

 




