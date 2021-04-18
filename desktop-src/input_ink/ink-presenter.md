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
# <a name="ink-presenter"></a><span data-ttu-id="ce9ac-103">Apresentador de tinta</span><span class="sxs-lookup"><span data-stu-id="ce9ac-103">Ink presenter</span></span>

<span data-ttu-id="ce9ac-104">As APIs do apresentador de tinta permitem que os aplicativos Microsoft Win32 gerenciem a entrada, o processamento e a renderização de entrada de tinta (padrão e modificado) por meio de um objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inserido na árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="ce9ac-105">A entrada por tinta padrão (dica de caneta ou dica/botão de borracha) não é modificada com uma unificação secundária, como um botão de rosca de caneta, botão direito do mouse ou semelhante.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="ce9ac-106">Os aplicativos Plataforma Universal do Windows (UWP) usando linguagem XAML (XAML) fornecem essa funcionalidade por meio de um controle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) junto com um objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) que se conecta à árvore visual [DirectComposition](../directcomp/directcomposition-portal.md) XAML.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="ce9ac-107">Para obter mais detalhes, consulte [interações de caneta e](/windows/uwp/design/input/pen-and-stylus-interactions)caneta.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="ce9ac-108">O [processador de tinta](ink-renderer.md) foi projetado para uso por desenvolvedores de aplicativos universais do Windows interessados em fornecer a funcionalidade [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) / [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) baseada em XAML em aplicativos nativos do Win32.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce9ac-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ce9ac-109">In this section</span></span>



| <span data-ttu-id="ce9ac-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="ce9ac-110">Topic</span></span>                                                               | <span data-ttu-id="ce9ac-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce9ac-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce9ac-112">Classes de apresentador de tinta</span><span class="sxs-lookup"><span data-stu-id="ce9ac-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="ce9ac-113">Os tópicos contidos nesta seção fornecem as especificações de referência para as classes de apresentador de tinta.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="ce9ac-114">Interfaces do apresentador de tinta</span><span class="sxs-lookup"><span data-stu-id="ce9ac-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="ce9ac-115">Os tópicos contidos nesta seção fornecem as especificações de referência para as interfaces do apresentador de tinta.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ce9ac-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce9ac-116">Related topics</span></span>

<span data-ttu-id="ce9ac-117">[Apresentador de tinta](ink-presenter.md), [interações de caneta e caneta](/windows/uwp/design/input/pen-and-stylus-interactions), [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="ce9ac-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
