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
# <a name="inkstart-method"></a><span data-ttu-id="bc6e2-103">Método InkStart</span><span class="sxs-lookup"><span data-stu-id="bc6e2-103">InkStart Method</span></span>

<span data-ttu-id="bc6e2-104">Os métodos **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usam construções de GUI do Win32, como contextos de dispositivo e objetos de caneta.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="bc6e2-105">Isso ilustra por que o CGuiPaper é necessário como um nível separado de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="bc6e2-106">Os aspectos de GUI do papel de desenho são tratados em CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="bc6e2-107">O objeto de copapel é enviado somente a dados de tinta.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="bc6e2-108">Outro motivo de design para o nível CGuiPaper de encapsulamento é a natureza dupla de seus métodos **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6e2-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="bc6e2-109">Eles não apenas chamam o copaper para registrar os dados de tinta conforme eles ocorrem, eles também pintam uma imagem visual do desenho conforme ele ocorre.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="bc6e2-110">CGuiPaper mantém um \_ sinalizador m bInkSaving para gerenciar essa natureza dupla.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="bc6e2-111">Quando m \_ bInkSaving é false, a imagem é desenhada na tela, mas os dados não são enviados para o copapel para gravação.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="bc6e2-112">Esse esquema é usado na repintura quando o usuário não está movendo o mouse, mas os dados de tinta do copapel estão sendo reenviados para CGuiPaper para repintura automático.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="bc6e2-113">CGuiPaper pode ser instruído a definir o \_ sinalizador m bInkSaving chamando seu método [**InkSaving**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6e2-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="bc6e2-114">Os trechos de código de exemplo a seguir ilustram os métodos **InkStart** de GUIPAPER. CPP E COLETOR. CPP.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="bc6e2-115">Método InkStart (GUIPAPER. CPP</span><span class="sxs-lookup"><span data-stu-id="bc6e2-115">InkStart Method (GUIPAPER.CPP)</span></span>


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



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="bc6e2-116">Método InkStart (coletor. CPP</span><span class="sxs-lookup"><span data-stu-id="bc6e2-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="bc6e2-117">O **StoClien** recebe os dados de desenho na forma de chamadas para a interface **IPaperSink** conectada em seu objeto COPaperSink.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="bc6e2-118">Esses métodos correspondem aos métodos **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) semelhantes em CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


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



<span data-ttu-id="bc6e2-119">Quando **InkStart** é chamado no coletor, ele chama CGuiPaper para desativar a gravação de tinta em copaper.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="bc6e2-120">O copaper não precisa receber uma cópia ecoada dos dados que está enviando.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="bc6e2-121">Quando [**InkDraw**](inkdraw-method.md) é chamado no coletor, ele simplesmente passa a chamada para **CGuiPaper:: InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="bc6e2-122">Quando [**InkStop**](cguipaper-methods.md) é chamado no coletor, CGuiPaper é chamado para ativar o salvamento de tinta novamente.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="bc6e2-123">O resultado é uma reprodução de dados de tinta de copapel para CGuiPaper somente para exibição.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="bc6e2-124">Você pode testar o comportamento de **StoClien** quando seu **IPaperSink** é desconectado escolhendo a opção de desconexão no menu do coletor.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="bc6e2-125">Como um experimento, depois de desconectar o coletor, escolha sobre no menu ajuda.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="bc6e2-126">Isso mostrará a caixa de diálogo sobre, que abordará parte do desenho do **StoClien**.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="bc6e2-127">Clique em OK na caixa de diálogo sobre.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="bc6e2-128">Observe que a parte do desenho que foi abordada agora não existe mais.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="bc6e2-129">Os dados de desenho não são perdidos, mas parte da imagem é.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="bc6e2-130">O cliente recebeu a mensagem do WM \_ Paint e emitiu o método [**IPaper:: redesenhar**](ipaper--redraw.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6e2-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="bc6e2-131">Mas como o coletor não estava conectado, ele não recebeu as chamadas **IPaperSink** para redesenhar o desenho.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="bc6e2-132">Você também pode testar esse comportamento minimizando o **StoClien** e, em seguida, restaurando-o.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="bc6e2-133">Nesse caso, toda a imagem de desenho é perdida e precisa de repintura.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="bc6e2-134">Para redesenhar a imagem de desenho após qualquer um desses testes, use o menu do coletor para se reconectar e, em seguida, escolha [**redesenhar**](ipaper--redraw.md) no menu desenhar.</span><span class="sxs-lookup"><span data-stu-id="bc6e2-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




