---
title: Comportamento de UAV com blocos não mapeados
description: O comportamento das leituras e gravações de modo de exibição de acesso não ordenado (UAV) depende do nível de suporte do hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916025"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="0d307-103">Comportamento de UAV com blocos não mapeados</span><span class="sxs-lookup"><span data-stu-id="0d307-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="0d307-104">O comportamento das leituras e gravações de modo de exibição de acesso não ordenado (UAV) depende do nível de suporte do hardware.</span><span class="sxs-lookup"><span data-stu-id="0d307-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="0d307-105">Para obter uma análise dos requisitos, consulte comportamento geral de leitura e gravação para [recursos](tiled-resources-features-tiers.md)de divisão de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d307-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="0d307-106">Esta seção resume o comportamento ideal.</span><span class="sxs-lookup"><span data-stu-id="0d307-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="0d307-107">As operações de sombreador que lêem a partir de um bloco não mapeado em um UAV retornam 0 em todos os componentes sem perder o formato e o padrão para componentes que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="0d307-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="0d307-108">As operações de sombreador que tentam gravar em um bloco não mapeado fazem com que nada seja gravado na área não mapeado (enquanto as gravações em uma área mapeada prosseguem).</span><span class="sxs-lookup"><span data-stu-id="0d307-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="0d307-109">Essa definição ideal para o tratamento de gravação não é exigida pelo [nível 2](tier-2.md); as gravações em blocos não mapeados podem acabar em um cache que pode ser coletado pelas leituras subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0d307-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d307-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d307-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d307-111">Acesso ao pipeline para recursos lado a lado</span><span class="sxs-lookup"><span data-stu-id="0d307-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




