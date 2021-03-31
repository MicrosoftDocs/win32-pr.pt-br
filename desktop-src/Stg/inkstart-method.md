---
title: Método InkStart
description: Os métodos InkStart, InkDraw e InkStop usam construções de GUI do Win32, como contextos de dispositivo e objetos de caneta.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916509"
---
# <a name="inkstart-method"></a>Método InkStart

Os métodos **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usam construções de GUI do Win32, como contextos de dispositivo e objetos de caneta. Isso ilustra por que o CGuiPaper é necessário como um nível separado de encapsulamento. Os aspectos de GUI do papel de desenho são tratados em CGuiPaper. O objeto de copapel é enviado somente a dados de tinta.

Outro motivo de design para o nível CGuiPaper de encapsulamento é a natureza dupla de seus métodos **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) . Eles não apenas chamam o copaper para registrar os dados de tinta conforme eles ocorrem, eles também pintam uma imagem visual do desenho conforme ele ocorre. CGuiPaper mantém um \_ sinalizador m bInkSaving para gerenciar essa natureza dupla. Quando m \_ bInkSaving é false, a imagem é desenhada na tela, mas os dados não são enviados para o copapel para gravação.

Esse esquema é usado na repintura quando o usuário não está movendo o mouse, mas os dados de tinta do copapel estão sendo reenviados para CGuiPaper para repintura automático. CGuiPaper pode ser instruído a definir o \_ sinalizador m bInkSaving chamando seu método [**InkSaving**](cguipaper-methods.md) .

Os trechos de código de exemplo a seguir ilustram os métodos **InkStart** de GUIPAPER. CPP E COLETOR. CPP.

## <a name="inkstart-method-guipapercpp"></a>Método InkStart (GUIPAPER. CPP


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a>Método InkStart (coletor. CPP

O **StoClien** recebe os dados de desenho na forma de chamadas para a interface **IPaperSink** conectada em seu objeto COPaperSink. Esses métodos correspondem aos métodos **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) semelhantes em CGuiPaper.


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



Quando **InkStart** é chamado no coletor, ele chama CGuiPaper para desativar a gravação de tinta em copaper. O copaper não precisa receber uma cópia ecoada dos dados que está enviando. Quando [**InkDraw**](inkdraw-method.md) é chamado no coletor, ele simplesmente passa a chamada para **CGuiPaper:: InkDraw**. Quando [**InkStop**](cguipaper-methods.md) é chamado no coletor, CGuiPaper é chamado para ativar o salvamento de tinta novamente. O resultado é uma reprodução de dados de tinta de copapel para CGuiPaper somente para exibição.

Você pode testar o comportamento de **StoClien** quando seu **IPaperSink** é desconectado escolhendo a opção de desconexão no menu do coletor. Como um experimento, depois de desconectar o coletor, escolha sobre no menu ajuda. Isso mostrará a caixa de diálogo sobre, que abordará parte do desenho do **StoClien**. Clique em OK na caixa de diálogo sobre. Observe que a parte do desenho que foi abordada agora não existe mais. Os dados de desenho não são perdidos, mas parte da imagem é. O cliente recebeu a mensagem do WM \_ Paint e emitiu o método [**IPaper:: redesenhar**](ipaper--redraw.md) . Mas como o coletor não estava conectado, ele não recebeu as chamadas **IPaperSink** para redesenhar o desenho.

Você também pode testar esse comportamento minimizando o **StoClien** e, em seguida, restaurando-o. Nesse caso, toda a imagem de desenho é perdida e precisa de repintura. Para redesenhar a imagem de desenho após qualquer um desses testes, use o menu do coletor para se reconectar e, em seguida, escolha [**redesenhar**](ipaper--redraw.md) no menu desenhar.

 

 




