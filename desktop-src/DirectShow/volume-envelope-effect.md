---
description: Efeito de envelope de volume
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Efeito de envelope de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761747"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="4c838-103">Efeito de envelope de volume</span><span class="sxs-lookup"><span data-stu-id="4c838-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="4c838-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4c838-104">\[Deprecated.</span></span> <span data-ttu-id="4c838-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c838-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c838-106">O efeito de envelope de volume define o volume em um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="4c838-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="4c838-107">ID de classe (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="4c838-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="4c838-108">Nome da variável CLSID: CLSID \_ AudMixer</span><span class="sxs-lookup"><span data-stu-id="4c838-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="4c838-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c838-109">Properties</span></span>



| <span data-ttu-id="4c838-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4c838-110">Property</span></span> | <span data-ttu-id="4c838-111">Type</span><span class="sxs-lookup"><span data-stu-id="4c838-111">Type</span></span>   | <span data-ttu-id="4c838-112">Padrão</span><span class="sxs-lookup"><span data-stu-id="4c838-112">Default</span></span> | <span data-ttu-id="4c838-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c838-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c838-114">Vol</span><span class="sxs-lookup"><span data-stu-id="4c838-114">Vol</span></span>      | <span data-ttu-id="4c838-115">double</span><span class="sxs-lookup"><span data-stu-id="4c838-115">double</span></span> | <span data-ttu-id="4c838-116">1.0</span><span class="sxs-lookup"><span data-stu-id="4c838-116">1.0</span></span>     | <span data-ttu-id="4c838-117">Volume, como uma porcentagem do volume criado.</span><span class="sxs-lookup"><span data-stu-id="4c838-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="4c838-118">Você pode produzir fades de áudio variando esse valor de propriedade ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="4c838-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4c838-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c838-119">Remarks</span></span>

<span data-ttu-id="4c838-120">Cada objeto em uma linha do tempo pode ter no máximo um efeito de envelope de volume.</span><span class="sxs-lookup"><span data-stu-id="4c838-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="4c838-121">Em uma composição ou grupo, o envelope de volume é aplicado primeiro, antes de qualquer outro efeito de áudio, independentemente de sua prioridade.</span><span class="sxs-lookup"><span data-stu-id="4c838-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="4c838-122">Em uma fonte ou um controle, o efeito do volume é aplicado de acordo com sua prioridade.</span><span class="sxs-lookup"><span data-stu-id="4c838-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



