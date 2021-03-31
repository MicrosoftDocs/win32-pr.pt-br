---
title: Níveis de proteção de saída
description: Níveis de proteção de saída
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- SDK do Windows Media Format, níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), OPL (níveis de proteção de saída)
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- níveis de proteção de saída (OPL)
- OPL (níveis de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e5c1e08615b55aa1fb63e6d0c4e7bb82887c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916036"
---
# <a name="output-protection-levels"></a><span data-ttu-id="e4075-108">Níveis de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="e4075-108">Output Protection Levels</span></span>

<span data-ttu-id="e4075-109">Os níveis de proteção de saída (OPLs) são classificações numéricas associadas a várias tecnologias que recebem conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="e4075-109">Output protection levels (OPLs) are numerical ratings associated with various technologies that receive digital media content.</span></span> <span data-ttu-id="e4075-110">O nível a que a tecnologia dá suporte depende de quão segura ela é.</span><span class="sxs-lookup"><span data-stu-id="e4075-110">The level a technology supports depends upon how secure it is.</span></span> <span data-ttu-id="e4075-111">O sistema OPL, introduzido no Windows Media DRM 10, permite que as licenças sejam criadas com mais flexibilidade do que nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="e4075-111">The OPL system, introduced in Windows Media DRM 10, enables licenses to be created with more flexibility than in previous versions.</span></span> <span data-ttu-id="e4075-112">Você pode especificar o mínimo de OPLs necessário para reprodução e para cópia.</span><span class="sxs-lookup"><span data-stu-id="e4075-112">You can specify minimum OPLs required for playback and for copying.</span></span> <span data-ttu-id="e4075-113">Além disso, você pode especificar exceções para o mínimo de OPL, para permitir que uma tecnologia não seja classificada como alta o suficiente ou para não permitir uma tecnologia com um OPL que exceda o mínimo.</span><span class="sxs-lookup"><span data-stu-id="e4075-113">In addition, you can specify exceptions to the minimum OPL, either to allow a technology not rated high enough, or to disallow a technology with an OPL that exceeds the minimum.</span></span>

<span data-ttu-id="e4075-114">Ao especificar restrições para licenças usando OPLs, um proprietário de conteúdo precisa usar apenas duas ações (copiar e reproduzir), em que as versões anteriores tinham ações separadas definidas para os vários tipos de dispositivos com suporte para cópia (SDMI, não SDMI e CD de áudio de livro vermelho).</span><span class="sxs-lookup"><span data-stu-id="e4075-114">By specifying restrictions to licenses using OPLs, a content owner need only use two actions (Copy and Play), where previous versions had separate actions defined for the various kinds of devices supported for copying (SDMI, non-SDMI, and Red Book audio CD).</span></span>

<span data-ttu-id="e4075-115">**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="e4075-115">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4075-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4075-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4075-117">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="e4075-117">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="e4075-118">**Trabalhando com níveis de proteção de saída**</span><span class="sxs-lookup"><span data-stu-id="e4075-118">**Working with Output Protection Levels**</span></span>](working-with-output-protection-levels.md)
</dt> </dl>

 

 




