---
description: Partições padrão
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Partições padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164163"
---
# <a name="default-partitions"></a><span data-ttu-id="cb655-103">Partições padrão</span><span class="sxs-lookup"><span data-stu-id="cb655-103">Default Partitions</span></span>

<span data-ttu-id="cb655-104">Quando uma partição padrão é atribuída a um usuário, o COM+ tenta ativar os componentes nessa partição primeiro.</span><span class="sxs-lookup"><span data-stu-id="cb655-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="cb655-105">Se a ativação falhar, o COM+ pesquisará a partição global do componente a ser ativado.</span><span class="sxs-lookup"><span data-stu-id="cb655-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="cb655-106">A exceção a esse processo ocorre quando o componente COM+ inclui um moniker de partição, que especifica explicitamente a partição na qual o componente está localizado.</span><span class="sxs-lookup"><span data-stu-id="cb655-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="cb655-107">Nesse caso, o moniker da partição tem precedência sobre qualquer configuração de partição padrão.</span><span class="sxs-lookup"><span data-stu-id="cb655-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="cb655-108">Ao usar partições locais, a partição padrão é atribuída aos usuários usando a pasta **usuários da partição com+** na ferramenta administrativa serviços de componentes no servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cb655-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="cb655-109">Ao usar conjuntos de partições no Active Directory, a partição padrão do usuário é determinada pelo conjunto de partições do usuário.</span><span class="sxs-lookup"><span data-stu-id="cb655-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb655-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb655-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb655-111">Partições locais</span><span class="sxs-lookup"><span data-stu-id="cb655-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="cb655-112">Propriedades da partição</span><span class="sxs-lookup"><span data-stu-id="cb655-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="cb655-113">Partições e Active Directory</span><span class="sxs-lookup"><span data-stu-id="cb655-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="cb655-114">A partição global</span><span class="sxs-lookup"><span data-stu-id="cb655-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



