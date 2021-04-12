---
title: Método InkDraw
description: CGuiPaper também mantém um \_ sinalizador m bInking. InkStart define como TRUE para sinalizar que uma sequência de desenho está em andamento. Por exemplo, o método InkDraw usa esse sinalizador para determinar se ele deve pintar e salvar dados de tinta.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364276"
---
# <a name="inkdraw-method"></a>Método InkDraw

CGuiPaper também mantém um \_ sinalizador m bInking. [InkStart](inkstart-method.md) define como **true** para sinalizar que uma sequência de desenho está em andamento. Por exemplo, o método InkDraw usa esse sinalizador para determinar se ele deve pintar e salvar dados de tinta.

A seguir está o método InkDraw de GUIPAPER. CPP.


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



Esse método não fará nada se m \_ bInking for **false**. Essa é a condição quando o usuário está simplesmente movendo o mouse sobre a janela do cliente sem pressionar o botão esquerdo do mouse.

InkDraw claramente tem uma responsabilidade dupla. As chamadas de MoveToEx e Linhato do Win32 são feitas para desenhar imagens de linha na tela da GUI (usando o identificador de contexto do dispositivo mantido em m \_ HDC). Os dados de tinta também são passados para o objeto de copapel para gravação usando o método InkDraw da interface [IPaper](ipaper-methods.md) . Quando m \_ bInkSaving for **false**, InkDraw pintará a imagem de linha, mas não armazenará os dados no copaper. Essa condição é usada durante a repintura.

 

 




