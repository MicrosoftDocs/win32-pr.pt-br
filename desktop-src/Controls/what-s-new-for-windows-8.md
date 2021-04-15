---
title: O que há de novo (controles do Windows)
description: Este tópico descreve as diferenças no suporte a temas e estilos visuais entre o Windows 8 e versões anteriores do Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454514"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="96139-103">O que há de novo (controles do Windows)</span><span class="sxs-lookup"><span data-stu-id="96139-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="96139-104">Este tópico descreve as diferenças no suporte a temas e estilos visuais entre o Windows 8 e versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="96139-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="96139-105">Por meio do Windows 7</span><span class="sxs-lookup"><span data-stu-id="96139-105">Through Windows 7</span></span>

<span data-ttu-id="96139-106">Com o Windows 7, os estilos visuais estão ativados por padrão, mas o usuário pode desativá-los selecionando o tema clássico do Windows ou desativando o serviço temas.</span><span class="sxs-lookup"><span data-stu-id="96139-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="96139-107">Quando os estilos visuais estão desativados, toda a interface do usuário Obtém a aparência clássica e a maioria das APIs de estilos visuais não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="96139-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="96139-108">O modo de estilos visuais foi mantido pelo Windows 7 para dar suporte a vários temas de alto contraste, bem como tema clássico do Windows.</span><span class="sxs-lookup"><span data-stu-id="96139-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="96139-109">Se você quiser dar suporte a estilos visuais e temas de alto contraste no mesmo aplicativo, normalmente precisará manter dois caminhos de código separados para renderizar controles.</span><span class="sxs-lookup"><span data-stu-id="96139-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="96139-110">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="96139-110">Windows 8 and Later</span></span>

<span data-ttu-id="96139-111">No Windows 8, os estilos visuais não podem ser desativados por meio da página **personalização** das **configurações do PC** ou pela desativação do serviço temas.</span><span class="sxs-lookup"><span data-stu-id="96139-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="96139-112">O modo clássico do Windows não existe mais e o modo de alto contraste foi modificado para funcionar com estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="96139-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="96139-113">Devido a essas alterações, os aplicativos que se destinam apenas ao Windows 8 não precisam mais de dois caminhos de código separados para dar suporte a estilos visuais e temas de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="96139-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="96139-114">Os estilos visuais no Windows 8 incluem suporte à compatibilidade com versões anteriores para o modo de tema clássico do Windows.</span><span class="sxs-lookup"><span data-stu-id="96139-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="96139-115">Qualquer código de renderização de interface do usuário que funcione em versões anteriores continuará funcionando no Windows 8 sem modificações.</span><span class="sxs-lookup"><span data-stu-id="96139-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="96139-116">No Windows 8, se você quiser que seu aplicativo dê suporte aos temas de alto contraste baseados em estilos visuais, você precisará incluir o GUID do Windows 8 na seção de compatibilidade do manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96139-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="96139-117">Caso contrário, o sistema pressupõe que o aplicativo foi projetado para uma versão anterior e renderiza a área do cliente simulando temas de alto contraste clássicos do Windows.</span><span class="sxs-lookup"><span data-stu-id="96139-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="96139-118">Para obter mais informações, consulte [suporte a temas de alto contraste](supporting-high-contrast-themes.md).</span><span class="sxs-lookup"><span data-stu-id="96139-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="96139-119">Como nas versões anteriores, o Windows 8 dá suporte à versão 5 e à versão 6 dos controles comuns, com a versão 5 sendo o padrão.</span><span class="sxs-lookup"><span data-stu-id="96139-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="96139-120">Como apenas a versão 6 dá suporte a estilos visuais, você deve especificar a versão 6 no manifesto do aplicativo se desejar que os estilos visuais sejam aplicados aos controles comuns na área do cliente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96139-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="96139-121">Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="96139-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96139-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96139-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96139-123">Habilitar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="96139-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="96139-124">Suporte a temas de Alto Contraste</span><span class="sxs-lookup"><span data-stu-id="96139-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="96139-125">Estilos visuais</span><span class="sxs-lookup"><span data-stu-id="96139-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="96139-126">Visão geral dos estilos visuais</span><span class="sxs-lookup"><span data-stu-id="96139-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




