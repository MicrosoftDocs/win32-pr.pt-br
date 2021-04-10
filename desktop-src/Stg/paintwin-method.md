---
title: Método PaintWin
description: Método PaintWin
ms.assetid: e89794e6-c059-4531-a1e3-3a4972e0218d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b30e7a52640255934762943f910e367d76088d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292875"
---
# <a name="paintwin-method"></a>Método PaintWin

A seguir está o método **PaintWin** da CGUIPAPER de GUIPAPER. CPP.


```C++
HRESULT CGuiPaper::PaintWin(void)
  {
    HRESULT hr = E_FAIL;
    COLORREF crInkColor;
    SHORT nInkWidth;

    if (m_pIPaper && !m_bPainting && !m_bInking)
    {
      m_bPainting = TRUE;
      // Save and restore ink color and width since redraw otherwise
      // ends up changing these values in CGuiPaper.
      crInkColor = m_crInkColor;
      nInkWidth = m_nInkWidth;
      hr = m_pIPaper->Redraw(m_nLockKey);
      m_nInkWidth = nInkWidth;
      m_crInkColor = crInkColor;
      m_bPainting = FALSE;
    }

    return hr;
  }
```



**PaintWin** essencialmente chama o método **redesenhar** do copaper. No exemplo de [StoServe](structured-storage-server-sample--stoserve-.md) , o método **redesenhar** foi mostrado para difundir a matriz de dados de tinta inteira do copapel para todos os coletores conectados. **PaintWin** chama um objeto no lado do servidor para enviar de volta os dados de desenho para o cliente.

 

 




