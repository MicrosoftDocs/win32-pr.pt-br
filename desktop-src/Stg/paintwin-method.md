---
title: Método PaintWin
description: Método PaintWin
ms.assetid: e89794e6-c059-4531-a1e3-3a4972e0218d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40708700ba4f0175713c59f6e3f1ff1395accadb0dcae3b31ca2e85862a998ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906026"
---
# <a name="paintwin-method"></a>Método PaintWin

A seguir está o método **PaintWin** de CGuiPaper do GUIPAPER. Cpp.


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



**O PaintWin** basicamente chama o método **Redraw** do COPaper. No exemplo [de StoServe,](structured-storage-server-sample--stoserve-.md) o método **Redraw** foi mostrado para transmitir toda a matriz de dados de tinta do COPaper para todos os sinks conectados. **PaintWin** chama um objeto no lado do servidor para enviar de volta os dados de desenho para o cliente.

 

 




