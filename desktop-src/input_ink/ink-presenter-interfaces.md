---
description: Os tópicos contidos nesta seção fornecem as especificações de referência para as interfaces do apresentador de tinta.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfaces do apresentador de tinta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808386"
---
# <a name="ink-presenter-interfaces"></a>Interfaces do apresentador de tinta

Os tópicos contidos nesta seção fornecem as especificações de referência para as interfaces do [apresentador de tinta](ink-presenter.md) .

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Permite que seu aplicativo (em vez de um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ) confirme todos os comandos do Microsoft DirectComposition pendentes na árvore visual do [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Permite entrada, processamento e renderização de tinta por meio da criação de um thread de aplicativo para hospedar um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inseri-lo na árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Representa uma operação de tinta a ser executada em um thread de objeto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) .<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Representa um [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) que pode ser configurado e inserido na árvore visual do [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo clássico do Windows. <br/>                                        |

## <a name="related-topics"></a>Tópicos relacionados

[Apresentador de tinta](ink-presenter.md), [interações de caneta e caneta](/windows/uwp/design/input/pen-and-stylus-interactions), [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)
