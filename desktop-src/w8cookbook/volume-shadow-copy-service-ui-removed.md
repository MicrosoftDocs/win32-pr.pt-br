---
title: Interface do usuário de versões anteriores removida para volumes locais
description: Interface do usuário de versões anteriores removida para volumes locais
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104454407"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="d71a7-103">Interface do usuário de versões anteriores removida para volumes locais</span><span class="sxs-lookup"><span data-stu-id="d71a7-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="d71a7-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="d71a7-104">Platform</span></span>

<span data-ttu-id="d71a7-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="d71a7-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="d71a7-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d71a7-106">Description</span></span>

<span data-ttu-id="d71a7-107">As versões anteriores do Windows permitiam que os usuários restaurassem versões anteriores de arquivos individuais de "cópias de sombra" de volumes locais.</span><span class="sxs-lookup"><span data-stu-id="d71a7-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="d71a7-108">Essas cópias de sombra são criadas pelo recurso "versões anteriores" por meio do VSS (serviço de cópias de sombra de volume).</span><span class="sxs-lookup"><span data-stu-id="d71a7-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="d71a7-109">No Windows 7, os usuários podem configurar e agendar cópias de sombra na interface do usuário de proteção do sistema disponível por meio de propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="d71a7-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="d71a7-110">No entanto, as versões anteriores eram raramente usadas e afetaram negativamente o desempenho geral do Windows; Como resultado, o recurso foi removido.</span><span class="sxs-lookup"><span data-stu-id="d71a7-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="d71a7-111">No Windows 8, esses recursos não estão mais disponíveis:</span><span class="sxs-lookup"><span data-stu-id="d71a7-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="d71a7-112">A capacidade de procurar, Pesquisar ou restaurar versões anteriores de arquivos por meio da interface do usuário de versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d71a7-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="d71a7-113">A capacidade de configurar ou agendar versões anteriores de arquivos por meio da interface do usuário de proteção do sistema</span><span class="sxs-lookup"><span data-stu-id="d71a7-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="d71a7-114">No entanto, os usuários ainda podem usar a guia versões anteriores ao acessar compartilhamentos de arquivos em um Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d71a7-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d71a7-115">Manifestação</span><span class="sxs-lookup"><span data-stu-id="d71a7-115">Manifestation</span></span>

<span data-ttu-id="d71a7-116">A opção de versões anteriores não está mais disponível para volumes locais no menu de propriedades do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d71a7-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="d71a7-117">Solução</span><span class="sxs-lookup"><span data-stu-id="d71a7-117">Solution</span></span>

<span data-ttu-id="d71a7-118">Os desenvolvedores que precisam criar cópias de sombra de volumes locais ainda podem fazer isso chamando APIs VSS em código personalizado.</span><span class="sxs-lookup"><span data-stu-id="d71a7-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 




