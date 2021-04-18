---
description: As APIs do apresentador de tinta permitem que os aplicativos do Microsoft Win32 gerenciem a entrada, o processamento e a renderização de entrada à tinta (padrão e modificada) por meio de um objeto InkPresenter inserido na árvore visual DirectComposition do aplicativo.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Apresentador de tinta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170526"
---
# <a name="ink-presenter"></a>Apresentador de tinta

As APIs do apresentador de tinta permitem que os aplicativos Microsoft Win32 gerenciem a entrada, o processamento e a renderização de entrada de tinta (padrão e modificado) por meio de um objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inserido na árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo.

> [!Note]
>
> A entrada por tinta padrão (dica de caneta ou dica/botão de borracha) não é modificada com uma unificação secundária, como um botão de rosca de caneta, botão direito do mouse ou semelhante.

Os aplicativos Plataforma Universal do Windows (UWP) usando linguagem XAML (XAML) fornecem essa funcionalidade por meio de um controle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) junto com um objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) que se conecta à árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) XAML. Para obter mais detalhes, consulte [interações de caneta e](/windows/uwp/design/input/pen-and-stylus-interactions)caneta.

O [processador de tinta](ink-renderer.md) foi projetado para uso por desenvolvedores de aplicativos universais do Windows interessados em fornecer a funcionalidade [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) / [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) baseada em XAML em aplicativos nativos do Win32.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                               | Descrição                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Classes de apresentador de tinta](ink-presenter-classes.md)<br/>       | Os tópicos contidos nesta seção fornecem as especificações de referência para as classes de apresentador de tinta. <br/>    |
| [Interfaces do apresentador de tinta](ink-presenter-interfaces.md)<br/> | Os tópicos contidos nesta seção fornecem as especificações de referência para as interfaces do apresentador de tinta. <br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

[Apresentador de tinta](ink-presenter.md), [interações de caneta e caneta](/windows/uwp/design/input/pen-and-stylus-interactions), [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)
