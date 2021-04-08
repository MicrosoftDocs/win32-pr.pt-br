---
description: Interdependências entre propriedades
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdependências entre propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920401"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="83bbb-103">Interdependências entre propriedades</span><span class="sxs-lookup"><span data-stu-id="83bbb-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="83bbb-104">Quando você define propriedades, o catálogo COM+ impõe alguma lógica de coerência para garantir que você configure elementos de forma razoável.</span><span class="sxs-lookup"><span data-stu-id="83bbb-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="83bbb-105">Essa lógica pode ser implementada de duas maneiras, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="83bbb-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="83bbb-106">**Depend.**</span><span class="sxs-lookup"><span data-stu-id="83bbb-106">**Dependencies.**</span></span> <span data-ttu-id="83bbb-107">Você pode estar impedido de fazer algumas alterações porque outra propriedade depende de uma configuração específica para uma propriedade que você tentar definir.</span><span class="sxs-lookup"><span data-stu-id="83bbb-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="83bbb-108">Por exemplo, se um componente for definido com as transações de atributo necessárias e se você tentar alterar a configuração de sincronização para nenhum, um erro será gerado quando você tentar chamar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) , pois as transações dependem da sincronização.</span><span class="sxs-lookup"><span data-stu-id="83bbb-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="83bbb-109">**Efeitos colaterais.**</span><span class="sxs-lookup"><span data-stu-id="83bbb-109">**Side effects.**</span></span> <span data-ttu-id="83bbb-110">Algumas propriedades podem ser alteradas sem que você as defina explicitamente.</span><span class="sxs-lookup"><span data-stu-id="83bbb-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="83bbb-111">Por exemplo, se você definir um componente com as transações de atributo necessárias, a sincronização será definida como obrigatória também.</span><span class="sxs-lookup"><span data-stu-id="83bbb-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="83bbb-112">Isso é realmente o lado inverso das dependências — uma propriedade tem precedência sobre outra, e sua dependência é expressa pela primeira configuração da propriedade secundária e, em seguida, pelo bloqueio das alterações nela.</span><span class="sxs-lookup"><span data-stu-id="83bbb-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="83bbb-113">Na lista de propriedades expostas por itens em uma coleção, todos listados em [coleções de administração com+](com--administration-collections.md), as dependências e os efeitos colaterais são declarados para cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="83bbb-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="83bbb-114">Ao configurar aplicativos e componentes COM+, você deve estar ciente das restrições que são impostas nas configurações.</span><span class="sxs-lookup"><span data-stu-id="83bbb-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83bbb-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83bbb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83bbb-116">Obtendo e definindo propriedades</span><span class="sxs-lookup"><span data-stu-id="83bbb-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="83bbb-117">Consultando as propriedades disponíveis</span><span class="sxs-lookup"><span data-stu-id="83bbb-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="83bbb-118">Salvando ou descartando alterações</span><span class="sxs-lookup"><span data-stu-id="83bbb-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



