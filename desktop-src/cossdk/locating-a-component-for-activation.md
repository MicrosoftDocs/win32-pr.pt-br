---
description: Localizando um componente para ativação
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Localizando um componente para ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104554837"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="04e4d-103">Localizando um componente para ativação</span><span class="sxs-lookup"><span data-stu-id="04e4d-103">Locating a Component for Activation</span></span>

<span data-ttu-id="04e4d-104">Quando o COM+ tiver localizado a partição correta — por meio do conjunto de partições padrão da identidade do usuário, um moniker da partição ou a ID da partição no contexto do objeto, COM + deverá localizar o componente correto dentro dessa partição.</span><span class="sxs-lookup"><span data-stu-id="04e4d-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="04e4d-105">A ilustração a seguir mostra como um componente é encontrado e ativado quando esse componente reside em uma partição.</span><span class="sxs-lookup"><span data-stu-id="04e4d-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="04e4d-106">Antes de qualquer ativação de componente, COM+ executa uma validação para verificar se a identidade do usuário que está tentando ativar o componente tem direitos para acessar o conjunto de partições no qual o componente reside.</span><span class="sxs-lookup"><span data-stu-id="04e4d-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![Diagrama que mostra uma árvore de solução de problemas para localizar um componente para ativação.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="04e4d-108">A ilustração anterior mostra o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04e4d-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="04e4d-109">Se o componente que está sendo chamado residir em uma partição e estiver no mesmo aplicativo que o componente de chamada, o componente será ativado se o componente que está sendo chamado estiver marcado como público ou privado.</span><span class="sxs-lookup"><span data-stu-id="04e4d-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="04e4d-110">Se o componente que está sendo chamado residir em uma partição, mas não existir no mesmo aplicativo que o componente de chamada, o COM+ verificará se o componente está marcado como público.</span><span class="sxs-lookup"><span data-stu-id="04e4d-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="04e4d-111">Se nenhuma versão pública for encontrada, o COM+ pesquisará a partição global para localizar uma versão pública do componente.</span><span class="sxs-lookup"><span data-stu-id="04e4d-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="04e4d-112">Se nenhuma versão pública do componente for encontrada na partição global ou se a identidade do usuário não tiver direitos para a partição, a ativação falhará.</span><span class="sxs-lookup"><span data-stu-id="04e4d-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04e4d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04e4d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04e4d-114">Localizando partições durante a ativação</span><span class="sxs-lookup"><span data-stu-id="04e4d-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 



