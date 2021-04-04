---
description: Definir essa política de sistema por usuário especifica a ordem em que o instalador pesquisa três tipos de fontes.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837403"
---
# <a name="searchorder"></a><span data-ttu-id="622e5-103">SearchOrder</span><span class="sxs-lookup"><span data-stu-id="622e5-103">SearchOrder</span></span>

<span data-ttu-id="622e5-104">Definir essa [política de sistema](system-policy.md) por usuário especifica a ordem em que o instalador pesquisa três tipos de fontes.</span><span class="sxs-lookup"><span data-stu-id="622e5-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="622e5-105">Os tipos de fontes são:</span><span class="sxs-lookup"><span data-stu-id="622e5-105">The types of sources are:</span></span>

<span data-ttu-id="622e5-106">"n" – rede</span><span class="sxs-lookup"><span data-stu-id="622e5-106">"n" – network</span></span>

<span data-ttu-id="622e5-107">"m" – mídia (CD-ROM ou DVD)</span><span class="sxs-lookup"><span data-stu-id="622e5-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="622e5-108">"u" – localizador de recursos uniforme (URL)</span><span class="sxs-lookup"><span data-stu-id="622e5-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="622e5-109">Por exemplo, para pesquisar fontes de rede primeiro, as fontes de mídia segundo e as fontes de URL foram definidas pela última vez essa política como um valor de "NMU".</span><span class="sxs-lookup"><span data-stu-id="622e5-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="622e5-110">Para omitir a pesquisa de um tipo de origem específico, deixe a letra correspondente do valor.</span><span class="sxs-lookup"><span data-stu-id="622e5-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="622e5-111">Se SearchOrder não for definido, a ordem de pesquisa padrão será Network, Media e, em seguida, URL.</span><span class="sxs-lookup"><span data-stu-id="622e5-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="622e5-112">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="622e5-112">Registry Key</span></span>

<span data-ttu-id="622e5-113">**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="622e5-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="622e5-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="622e5-114">Data Type</span></span>

<span data-ttu-id="622e5-115">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="622e5-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="622e5-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="622e5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="622e5-117">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="622e5-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



