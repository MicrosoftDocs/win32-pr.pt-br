---
title: DirectComposition
description: Este tópico explica a finalidade do Microsoft DirectComposition, identifica seus requisitos de tempo de execução e descreve o plano de fundo de programação que você precisa para usar o Microsoft DirectComposition com eficiência.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- DirectComposition Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291984"
---
# <a name="directcomposition"></a><span data-ttu-id="26e3a-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26e3a-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="26e3a-107">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="26e3a-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="26e3a-108">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="26e3a-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="26e3a-109">Finalidade</span><span class="sxs-lookup"><span data-stu-id="26e3a-109">Purpose</span></span>

<span data-ttu-id="26e3a-110">O Microsoft DirectComposition é um componente do Windows que permite a composição de bitmap de alto desempenho com transformações, efeitos e animações.</span><span class="sxs-lookup"><span data-stu-id="26e3a-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="26e3a-111">Os desenvolvedores de aplicativos podem usar a API DirectComposition para criar interfaces do usuário visualmente atraentes que contam com transições animadas avançadas e fluidas de um elemento visual para outro.</span><span class="sxs-lookup"><span data-stu-id="26e3a-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="26e3a-112">O DirectComposition permite transições avançadas e fluintes obtendo uma alta taxa de quadros, usando hardware de gráficos e operando independentemente do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="26e3a-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="26e3a-113">O DirectComposition pode aceitar conteúdo de bitmap desenhado por diferentes bibliotecas de renderização, incluindo bitmaps do Microsoft DirectX e bitmaps renderizados para uma janela (bitmaps HWND).</span><span class="sxs-lookup"><span data-stu-id="26e3a-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="26e3a-114">Além disso, o DirectComposition dá suporte a uma variedade de transformações, como transformações de afinidade 2D e transformações de perspectiva 3D, bem como efeitos básicos como recorte e opacidade.</span><span class="sxs-lookup"><span data-stu-id="26e3a-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="26e3a-115">O DirectComposition foi projetado para simplificar o processo de composição de [*visuais*](directcomposition-glossary.md) e criação de transições animadas.</span><span class="sxs-lookup"><span data-stu-id="26e3a-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="26e3a-116">Se seu aplicativo já contiver código de renderização ou já usar a API do DirectX recomendada, você só precisará fazer uma quantidade mínima de trabalho para usar o DirectComposition efetivamente.</span><span class="sxs-lookup"><span data-stu-id="26e3a-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="26e3a-117">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="26e3a-117">Developer audience</span></span>

<span data-ttu-id="26e3a-118">A API do DirectComposition destina-se a desenvolvedores de gráficos experientes e altamente compatíveis que conhecem o C/C++, têm uma compreensão sólida do COM (Component Object Model) e estão familiarizados com os conceitos de programação do Windows.</span><span class="sxs-lookup"><span data-stu-id="26e3a-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="26e3a-119">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="26e3a-119">Run-time requirements</span></span>

<span data-ttu-id="26e3a-120">O DirectComposition foi introduzido no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="26e3a-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="26e3a-121">Ele está incluído em plataformas de 32 bits, 64 bits e ARM.</span><span class="sxs-lookup"><span data-stu-id="26e3a-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="26e3a-122">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="26e3a-122">In this section</span></span>



| <span data-ttu-id="26e3a-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="26e3a-123">Topic</span></span>                                                                       | <span data-ttu-id="26e3a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="26e3a-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26e3a-125">Por que usar o DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="26e3a-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="26e3a-126">Este tópico descreve os recursos e os benefícios do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="26e3a-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="26e3a-127">Como usar o DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26e3a-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="26e3a-128">Esta seção descreve as práticas recomendadas para usar a API DirectComposition e demonstra como usar a API para realizar várias tarefas comuns.</span><span class="sxs-lookup"><span data-stu-id="26e3a-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="26e3a-129">Conceitos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26e3a-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="26e3a-130">Esta seção fornece uma visão geral conceitual do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="26e3a-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="26e3a-131">Referência de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26e3a-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="26e3a-132">Esta seção fornece informações de referência detalhadas para os elementos que compõem a API DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="26e3a-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="26e3a-133">Exemplos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26e3a-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="26e3a-134">Os aplicativos de exemplo a seguir mostram como usar a API DirectComposition e demonstrar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="26e3a-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="26e3a-135">Glossário do DirectComposition</span><span class="sxs-lookup"><span data-stu-id="26e3a-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="26e3a-136">Este tópico define os termos de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="26e3a-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





