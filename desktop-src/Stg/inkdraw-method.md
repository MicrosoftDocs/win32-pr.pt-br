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
# <a name="inkdraw-method"></a><span data-ttu-id="3cfc0-106">Método InkDraw</span><span class="sxs-lookup"><span data-stu-id="3cfc0-106">InkDraw Method</span></span>

<span data-ttu-id="3cfc0-107">CGuiPaper também mantém um \_ sinalizador m bInking.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-107">CGuiPaper also keeps an m\_bInking flag.</span></span> <span data-ttu-id="3cfc0-108">[InkStart](inkstart-method.md) define como **true** para sinalizar que uma sequência de desenho está em andamento.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-108">[InkStart](inkstart-method.md) sets it to **TRUE** to signal that a drawing sequence is in process.</span></span> <span data-ttu-id="3cfc0-109">Por exemplo, o método InkDraw usa esse sinalizador para determinar se ele deve pintar e salvar dados de tinta.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-109">For example, the InkDraw method uses this flag to determine whether it should paint and save ink data.</span></span>

<span data-ttu-id="3cfc0-110">A seguir está o método InkDraw de GUIPAPER. CPP.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-110">The following is the InkDraw method from GUIPAPER.CPP.</span></span>


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



<span data-ttu-id="3cfc0-111">Esse método não fará nada se m \_ bInking for **false**.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-111">This method does nothing if m\_bInking is **FALSE**.</span></span> <span data-ttu-id="3cfc0-112">Essa é a condição quando o usuário está simplesmente movendo o mouse sobre a janela do cliente sem pressionar o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-112">This is the condition when the user is simply moving the mouse over the client window without pressing the left mouse button.</span></span>

<span data-ttu-id="3cfc0-113">InkDraw claramente tem uma responsabilidade dupla.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-113">InkDraw clearly has a dual responsibility.</span></span> <span data-ttu-id="3cfc0-114">As chamadas de MoveToEx e Linhato do Win32 são feitas para desenhar imagens de linha na tela da GUI (usando o identificador de contexto do dispositivo mantido em m \_ HDC).</span><span class="sxs-lookup"><span data-stu-id="3cfc0-114">The Win32 MoveToEx and LineTo calls are made to draw line images on the GUI screen (using the device context handle kept in m\_hDC).</span></span> <span data-ttu-id="3cfc0-115">Os dados de tinta também são passados para o objeto de copapel para gravação usando o método InkDraw da interface [IPaper](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfc0-115">The ink data is also passed to the COPaper object for recording using the [IPaper](ipaper-methods.md) interface's InkDraw method.</span></span> <span data-ttu-id="3cfc0-116">Quando m \_ bInkSaving for **false**, InkDraw pintará a imagem de linha, mas não armazenará os dados no copaper.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-116">When m\_bInkSaving is **FALSE**, InkDraw paints the line image but does not store the data in COPaper.</span></span> <span data-ttu-id="3cfc0-117">Essa condição é usada durante a repintura.</span><span class="sxs-lookup"><span data-stu-id="3cfc0-117">This condition is used during repainting.</span></span>

 

 




