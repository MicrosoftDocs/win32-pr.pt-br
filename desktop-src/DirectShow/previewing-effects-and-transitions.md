---
description: Visualização de efeitos e transições
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Visualização de efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087792"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="ad314-103">Visualização de efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="ad314-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="ad314-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="ad314-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="ad314-105">Alguns efeitos e transições levam um tempo relativamente longo para serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="ad314-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="ad314-106">Durante a visualização, isso pode fazer com que o vídeo se torne instável ou fora de sincronia com o áudio.</span><span class="sxs-lookup"><span data-stu-id="ad314-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="ad314-107">Você pode aumentar a velocidade de visualização desabilitando efeitos ou transições:</span><span class="sxs-lookup"><span data-stu-id="ad314-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="ad314-108">Para desabilitar todos os efeitos, chame [**IAMTimeline:: EnableEffects**](iamtimeline-enableeffects.md).</span><span class="sxs-lookup"><span data-stu-id="ad314-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="ad314-109">Para desabilitar todas as transições, chame [**IAMTimeline:: EnableTransitions**](iamtimeline-enabletransitions.md).</span><span class="sxs-lookup"><span data-stu-id="ad314-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="ad314-110">Para desabilitar uma transição específica, chame [**IAMTimelineTrans:: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span><span class="sxs-lookup"><span data-stu-id="ad314-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="ad314-111">Quando os efeitos são desabilitados, eles não são renderizados durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="ad314-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="ad314-112">Quando uma transição é desabilitada, ela é renderizada como um corte de salto.</span><span class="sxs-lookup"><span data-stu-id="ad314-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="ad314-113">O transição entre faixas ainda ocorre, mas o efeito visual não é renderizado.</span><span class="sxs-lookup"><span data-stu-id="ad314-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="ad314-114">Se um efeito ou uma transição não puder ser renderizado, o mecanismo de renderização substituirá um efeito ou uma transição padrão.</span><span class="sxs-lookup"><span data-stu-id="ad314-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="ad314-115">Chame o método [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) para definir o efeito padrão e o método [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) para definir a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="ad314-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="ad314-116">Se você não especificar um padrão, ou se aquele que você especificar também causar um erro, o DES usará seu próprio padrão.</span><span class="sxs-lookup"><span data-stu-id="ad314-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="ad314-117">Você também pode melhorar a qualidade da visualização aumentando a quantidade de buffers de quadros.</span><span class="sxs-lookup"><span data-stu-id="ad314-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="ad314-118">Consulte [**IAMTimelineGroup:: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span><span class="sxs-lookup"><span data-stu-id="ad314-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ad314-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad314-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad314-120">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="ad314-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



