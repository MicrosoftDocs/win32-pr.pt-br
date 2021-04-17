---
description: Saiba mais sobre as várias APIs de tinta de área de trabalho para aplicativos do Windows.
ms.assetid: 0691afb1-575a-4bb7-8fa5-006b231b8f1f
title: Entrada à tinta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ffb67d452e3bee327195f8ff920bfcab3c0232a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790651"
---
# <a name="ink-input"></a><span data-ttu-id="a792c-103">Entrada à tinta</span><span class="sxs-lookup"><span data-stu-id="a792c-103">Ink input</span></span>

<span data-ttu-id="a792c-104">Saiba mais sobre as várias APIs de tinta de área de trabalho para aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="a792c-104">Learn about the various Desktop inking APIs for Windows apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a792c-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a792c-105">In this section</span></span>

| <span data-ttu-id="a792c-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="a792c-106">Topic</span></span> | <span data-ttu-id="a792c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a792c-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="a792c-108">Apresentador de tinta</span><span class="sxs-lookup"><span data-stu-id="a792c-108">Ink presenter</span></span>](ink-presenter.md)<br/> | <span data-ttu-id="a792c-109">As APIs do apresentador de tinta permitem que os aplicativos Microsoft Win32 gerenciem a entrada, o processamento e a renderização de entrada de tinta (padrão e modificado) por meio de um objeto [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) inserido na árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a792c-109">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span><br/> |
| [<span data-ttu-id="a792c-110">Processador de tinta</span><span class="sxs-lookup"><span data-stu-id="a792c-110">Ink renderer</span></span>](ink-renderer.md)<br/>   | <span data-ttu-id="a792c-111">As APIs do [processador de tinta](ink-renderer.md) permitem a renderização de traços de tinta no contexto do dispositivo Direct2D designado de um aplicativo universal do Windows, em vez do controle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) padrão.</span><span class="sxs-lookup"><span data-stu-id="a792c-111">The [Ink renderer](ink-renderer.md) APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span><br/>                                                                        |

## <a name="related-topics"></a><span data-ttu-id="a792c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a792c-112">Related topics</span></span>

<span data-ttu-id="a792c-113">[Interações de caneta e](/windows/uwp/design/input/pen-and-stylus-interactions)caneta, exemplo de [análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), [exemplo de escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="a792c-113">[Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
