---
description: O administrador do sistema pode definir cotas para usuários específicos em um volume. O administrador também pode definir as cotas padrão para o volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Administração em nível de sistema de cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164643"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="aa856-104">Administração em nível de sistema de cotas de disco</span><span class="sxs-lookup"><span data-stu-id="aa856-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="aa856-105">O administrador do sistema pode definir cotas para usuários específicos em um volume.</span><span class="sxs-lookup"><span data-stu-id="aa856-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="aa856-106">O administrador também pode definir as cotas padrão para o volume.</span><span class="sxs-lookup"><span data-stu-id="aa856-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="aa856-107">Um novo usuário no volume recebe a cota padrão, a menos que o administrador tenha estabelecido uma cota especificamente para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="aa856-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="aa856-108">O administrador pode consultar o nível de controle de cotas e imposição (ou Estados de cota), os limites de cota padrão e as informações de cota por usuário.</span><span class="sxs-lookup"><span data-stu-id="aa856-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="aa856-109">As informações de cota por usuário contêm o limite de cota rígido do usuário, o limite de aviso e o uso da cota.</span><span class="sxs-lookup"><span data-stu-id="aa856-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="aa856-110">O administrador também pode habilitar ou desabilitar a imposição de cotas.</span><span class="sxs-lookup"><span data-stu-id="aa856-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="aa856-111">Há três Estados de cota, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa856-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="aa856-112">Estado</span><span class="sxs-lookup"><span data-stu-id="aa856-112">State</span></span>          | <span data-ttu-id="aa856-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa856-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa856-114">Cota desabilitada</span><span class="sxs-lookup"><span data-stu-id="aa856-114">Quota disabled</span></span> | <span data-ttu-id="aa856-115">As alterações de uso de cota não são rastreadas, mas os limites de cota não são removidos.</span><span class="sxs-lookup"><span data-stu-id="aa856-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="aa856-116">Nesse estado, o desempenho não é afetado pelas cotas de disco.</span><span class="sxs-lookup"><span data-stu-id="aa856-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="aa856-117">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="aa856-117">This is the default state.</span></span>                         |
| <span data-ttu-id="aa856-118">Cota controlada</span><span class="sxs-lookup"><span data-stu-id="aa856-118">Quota tracked</span></span>  | <span data-ttu-id="aa856-119">As alterações de uso de cota são controladas, mas os limites de cota não são impostos.</span><span class="sxs-lookup"><span data-stu-id="aa856-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="aa856-120">Nesse estado, nenhum evento de violação de cota é gerado e nenhuma operação de arquivo falha devido a violações de cota de disco.</span><span class="sxs-lookup"><span data-stu-id="aa856-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="aa856-121">Cota imposta</span><span class="sxs-lookup"><span data-stu-id="aa856-121">Quota enforced</span></span> | <span data-ttu-id="aa856-122">As alterações de uso de cota são rastreadas e os limites de cota são impostos.</span><span class="sxs-lookup"><span data-stu-id="aa856-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



