---
title: Gravando um CD
description: Gravando um CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, sobre
- gravando CDs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084360"
---
# <a name="burning-a-cd"></a>Gravando um CD

Esta seção descreve como usar a interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) para gravar música em um CD. A interface **IWMPCdromBurn** fornece funcionalidade para gravar listas de reprodução em CDs como faixas de dados ou áudio, bem como apagar a CD-RWs.

Uso de código

Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.

Cabeçalhos incluídos

Para usar o código nesta seção, inclua os seguintes cabeçalhos:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Ponteiros de interface

As interfaces do Windows Media Player são armazenadas nas seguintes variáveis de membro:


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
-   [Iniciando o processo de gravação](starting-the-burn-process.md)
-   [Apagando um CD regravável](erasing-a-rewritable-cd.md)
-   [Recuperando a unidade e o status do disco](retrieving-the-drive-and-disc-status.md)
-   [Recuperando o status da gravação](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de controle do Player**](player-control-guide.md)
</dt> </dl>

 

 




