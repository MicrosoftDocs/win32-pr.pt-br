---
title: Iniciando o processo de RIP
description: Iniciando o processo de RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, iniciando processo de RIP
- copiando CDs, iniciando processo RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105811400"
---
# <a name="starting-the-rip-process"></a>Iniciando o processo de RIP

Depois de recuperar a interface de cópia de música conforme explicado na seção anterior, inicie o processo de cópia de CDs chamando [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



Você pode interromper a operação de cópia de CDs chamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperar a interface de extração**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Recuperando o status do RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selecionando itens para copiar**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




