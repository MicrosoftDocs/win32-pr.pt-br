---
description: Os tópicos contidos nesta seção fornecem as especificações de referência para interfaces de apresentador de tinta.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfaces do apresentador de tinta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0c1fb4cab0b8387dec7c75087a72719f72fbc85dc2776a5e20fc6d638fb02d95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092386"
---
# <a name="ink-presenter-interfaces"></a>Interfaces do apresentador de tinta

Os tópicos contidos nesta seção fornecem as especificações de referência para interfaces [de apresentador de](ink-presenter.md) tinta.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Habilita seu aplicativo (em vez de um objeto [**IInkPresenterDesktop)**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) a fazer commit de todos os comandos do Microsoft DirectComposition pendentes na árvore visual [DirectComposition do](../directcomp/directcomposition-portal.md) aplicativo.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Habilita a entrada, o processamento e a renderização de tinta por meio da criação de um thread de aplicativo para hospedar um objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inseri-lo na árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Representa uma operação de tinta a ser executada em um thread [**de objeto IInkDesktopHost.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Representa um [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) que pode ser configurado e inserido na árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo Windows Clássico. <br/>                                        |

## <a name="related-topics"></a>Tópicos relacionados

[Apresentador de tinta,](ink-presenter.md) [interações de caneta](/windows/uwp/design/input/pen-and-stylus-interactions)e caneta, exemplo de Análise de [Tinta,](/samples/microsoft/windows-universal-samples/inkanalysis/)Exemplo de tinta [simples,](/samples/microsoft/windows-universal-samples/simpleink/) [Amostra de tinta complexa](/samples/microsoft/windows-universal-samples/complexink/)
